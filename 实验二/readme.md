# 实验二 DDA直线生成算法
## 时间：2022年3月23日  地点：信息学院2202机房
## 内容：熟悉OpenGL，通过DDA、中点算法生成直线段
## 目的：安装OpenGL，能编写代码运行，参考课本代码。  初步熟悉OpenGL编程及其编程框架；  熟悉OpenGL，通过示例程序生成直线段等图元

`<  void lineDDA(int x0,int y0,int xEnd,int yEnd)
{
    glClear(GL_COLOR_BUFFER_BIT);// 清空显示窗口
    glColor3f(0.0, 0.4, 0.2);// 指定前景色（当前绘制颜色）为蓝色

    int dx=xEnd-x0,dy=yEnd-y0,steps,k;
    float xIncrement,yIncrement,x=x0,y=y0;

    if(abs(dx)>abs(dy))
        steps = abs(dy);
    else
        steps = abs(dx);
    xIncrement = float(dx)/float(steps);
    yIncrement = float (dy)/float(steps);

    setPixel(round(x),round(y));
    for (k=0;k<steps;k++)
    {
        x+=xIncrement;
        y+=yIncrement;
        setPixel(round(x),round(y));
    }
}>` 
![image](https://github.com/Polaris1491319352/Graphics/blob/main/image/DDA.jpg)
