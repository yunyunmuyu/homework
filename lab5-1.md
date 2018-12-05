贪吃蛇游戏：


#include<stdio.h>

char map[12][12]=
{"************"
 "*XXXXH     *"
 "*          *"
 "*          *"
 "*          *"
 "*          *"
 "*          *"
 "*          *"
 "*          *"
 "*          *"
 "*          *"
 "************"
}
 struct point{
 int x;
 int y;
 }points[5]={
 	1,1,
 	2,1,
 	3,1,
 	4,1,
 	5,1,
 };
 void snakemove(char c)
 {
 	int i;
 	for(i=0;i<4;++i)
 	{
 		points[i].x=points[i+1].x;
 		points[i].y=points[i+1].y;
	 }
   switch(c){
   	case 'A':points[4].x--;    break；   
	case 'D' : points[4].x++;  	break;
	case 'S' :points[4].y++;   break;
	case 'W' :points[4].y--;  break ;
	   }
}
int  gameover(char c){
	switch(c){
   	case 'A':x=points[4].x-1,y=points[4].y;    break；   
	case 'D' :x=points[4].x+1; y=points[4].y;  	break;
	case 'S' :y=points[4].y+1; x=points[4].x  ;break;
	case 'W' :y=points[4].y-1; x=points[4].x ;break ;
	   }
	if(map[y][x]=='*')
	  return -1;
	  else return 1;
}
void output()
{ 
    int i,j,n=0;
	map[points[0].y][points[0].x]='X';
	map[points[1].y][points[1].x]='X';
	map[points[2].y][points[2].x]='X';
	map[points[3].y][points[3].x]='X';
	map[points[4].y][points[4].x]='H';
	for(i=0;i<12;++i)
	   for(j=0;j<12;++j)
	   {
	   	printf("%c",map[i][j]);
	   	++n;
	   	if(n%12==0)   printf("\n")
	   }
}
int main()
{
	char c;
	scanf("%c",&c);
	if(gameover(c)==-1)
	    goto end;
	snakemove(c);
	output(map);
	end: printf("GAMEOVER");
}

 	
 

