计算机中的颜色表示 ：
一、RGB颜色模式

RGB颜色模式是一种加色模式，图像使用红Red、绿Green、蓝Blue3种颜色分量，图像中每个像素的每种颜色分量可取从0黑色~255白色范围的强度值，其混合颜色即为该香像素的颜色，多达1670万种。绝大部分的可见光谱可以用红、绿、蓝RGB三色光按不同比例和强度的混合来表示，这种颜色模式主要用于计算机显示.
![](https://img-blog.csdn.net/20171116082813320?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2luYXRfMjAwMTk1MTE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)
 二、HSV颜色模式 

       在计算机中的实际应用中，除了RGB表示方法外，还有一种用的比较多的表示方法就是HSV（又称HSB）表示方法。它把颜色分为三个参量，一个是色相Hue，具体表示在色相环上的一种纯色，一个是饱和Saturation，具体表示纯色在颜色中的百分比，当S=1时，表示颜色最纯，当S=0时，表示灰度值。一个是亮度Value，表示颜色的亮度，当V=0时，表示黑色。

      HSV颜色系统在不破坏图像结构的基础上更该颜色方面起着不小的作用。比方说，我们在网上看到一种按钮设计觉得非常好，但是他的颜色不符合我们的要求，我们可以模仿他的样式，自己重新制作一个按钮，不过由于美术功底不足，无论怎么调整都做不出原来的感觉来。原因就是原来的按钮各种颜色搭配是有一定的道理的，自己重新选择颜色感觉就是不协调。我们可以利用HSV，直接更改按钮的各个颜色的色相值，这样由于是整体更改颜色的色相值，各种颜色搭配还是比较协调的。
![](https://img-blog.csdn.net/20171116083622779?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2luYXRfMjAwMTk1MTE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center).
三、CMYK颜色模式 
CMYK颜色模式是一种减色模式，主要用于印刷。C（Cyan）代表青色，M（Msgenta）代表品红色，Y（Yellow）代表黄色，K（Black）代表黑色。CMY 分别是红、绿、蓝的互补色，由于这3种颜色混合在一起只能得到暗棕色，而不是真正的黑色，所以另外引入了黑色。在CMYK图像中，当所有的分量的值都是0%时，会产生纯白色。当用印刷色打印制作的图像时，使用CMYK颜色模式。
  ![](https://img-blog.csdn.net/20171116083848040?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2luYXRfMjAwMTk1MTE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)
  四、Lab颜色模式 

Lab颜色模式的颜色设计与设备无关，不管是什么设备（如打印机、扫描仪或显示器）创建或输出图像。这种颜色模式产生的颜色都保持一致。 
![](https://img-blog.csdn.net/20171116084023989?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2luYXRfMjAwMTk1MTE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)