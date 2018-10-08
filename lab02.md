   
   
                使用construct2制作游戏的教程

一 准备：
下载construct2 
 https://www.scirra.com/construct2

 下载游戏素材：背景图片

 ![](https://www.scirra.com/images/articles/bg.png)

 player:
  
  ![](https://www.scirra.com/images/articles/player.png)

  monster:
   
   ![](https://www.scirra.com/images/articles/monster.png)

   bullet:

   ![](https://www.scirra.com/images/articles/Bullet.png)
  
   explosion:


  ![](https://www.scirra.com/images/articles/explode.png)


  二 增加布局层数
  打开construct2，点击文件开启新的文件。
  再点击右边的方框开启一个新的layout


  三  设置背景
双击空白处，将出现菜单如图:
![](https://github.com/yunyunmuyu/homeworkjw/blob/gh-pages/images/2345%E6%88%AA%E5%9B%BE20181006174850.png)

 双击Tiled background：打开文件，选择下载好的背景图片，打开
  调节图片的大小，通过调节左方框内的size项目调节一般为4000，4000；
  或者通过ctrl键调节

四 设置人物
 点击鼠标右键，选择加入新的项目，将出现方框，双击sptite，选择添加player等；monster项目应当增加多个到layout里面。
 项目添加完后要设置项目的动作：
 以player为例：
 在右下方框内点击player的图标，再到左方框内找到behaviors，点击。
再点击加号的标志，将会出现如图所示的方框：

！[](https://github.com/yunyunmuyu/homeworkjw/blob/gh-pages/images/2345%E6%88%AA%E5%9B%BE20181006175538.png)

选择8direction，boundTolayout,ScrollTo三个动作。
相应的给monster设置bullet movement动作，并在左方框把速度设置为500；
bullet增加bullet movement和destroy outside layout 动作；


五：编写事件
事件一，令player朝向鼠标
 首先我们要新增加鼠标项目，然后
点击Event sheet，再双击空白页面，将会出现方框


！[](https://github.com/yunyunmuyu/homeworkjw/blob/gh-pages/images/2345%E6%88%AA%E5%9B%BE20181006182132.png)
 点击system>>every tick>>add action>>player>>set angle toward position>>
将会出现一个新的方框，点击mouse，相应的选择X，Y；如图
！[](https://github.com/yunyunmuyu/homeworkjw/blob/gh-pages/images/2345%E6%88%AA%E5%9B%BE20181006184800.png).
 这样我们的第一个事件就设置好了

 事件二：让player射击
 右键增加事件>>mouse>>On Left button Clicked>>add action>>player>>spawn another object将出现如图的界面

 ！[](https://github.com/yunyunmuyu/homeworkjw/blob/gh-pages/images/2345%E6%88%AA%E5%9B%BE20181006211631.png)

 选择bullet项目 ，设置layer1，image point 1；
 下面，我们要设置子弹的发射位置，右击player项目，选择Edit animations，在
 打开的方框里选择准星的图标

 ！[](https://github.com/yunyunmuyu/homeworkjw/blob/gh-pages/images/2345%E6%88%AA%E5%9B%BE20181006211841.png)
  
然后点击player的发射位置保存。
  
  事件三：
  让子弹攻击moknster，
  Condition: Bullet -> On collision with another object -> pick Monster.
Action: Monster -> Destroy
Action: Bullet -> Spawn another object -> Explosion, layer 1
Action: Bullet -> Destroy

这时，如果我们运行游戏，会发现爆炸图片的图标背景为黑色，我们要把黑背景去掉。点击explosion图标，在左方框找到effect的目录。

！[](https://github.com/yunyunmuyu/homeworkjw/blob/gh-pages/images/2345%E6%88%AA%E5%9B%BE20181006212840.png)

更改Blend mode 为Addictive。

事件四：让monster随机运动

system>>on start of layout >>monnster>>set angle to random(360) degrees。




六  增加monster的血条：
点击monster，在左方框点击instance variable,点击增加，
name：health   type：number    initial value:5

！[](https://github.com/yunyunmuyu/homeworkjw/blob/gh-pages/images/2345%E6%88%AA%E5%9B%BE20181006221641.png)
  

然后在Bullet - on collision with Monster，的后面将monster destroy 的动作更改：右键点击该动作，选择replace action，选择Monster -> Subtract from (in the Instance variables category) -> Instance variable "health"

在这里我们要增加事件五：
事件五：
Monster -> Compare instance variable -> Health, Less or equal, 0
Action: Monster -> Spawn another object -> Explosion, layer 1
Action: Monster -> Destroy，


到了这里，一个小游戏就被我们制作出来啦，小伙伴们赶紧享受一下自己制作的游戏吧！！！！！




