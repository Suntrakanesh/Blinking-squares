
#include<stdio.h>
#include<conio.h>
#include<graphics.h>
#include<dos.h>
#include<stdlib.h>
void load(); 
void main()
{

randomize();
int gd=DETECT,gm,a,b,c,d,e,f,i,k=1,j=7,l;
int m,n,o;
initgraph(&gd,&gm,"c:\\Turboc3\\bgi");
a=getmaxx()/27;
b=getmaxy()/2; 
setbkcolor(RED); 
settextstyle(0,0,4) outtextxy(a,b,"\2BLINKING SQUARES\2");
delay(2000); 
cleardevice();
load(); 
cleardevice(); 


x: 
clrscr();
k=k+1;
j=j-1; 
c=rand()%4;
d=rand()%3; 
e=rand()%4;
f=rand()%3;

for(i=0;i<=c;i++)

{
setfillstyle(1,RED); 
rectangle(210,105,310,205);
floodfill(215,110,RED);
delay(j*100); setfillstyle(1,5); 
rectangle(210,105,310,205);
floodfill(215,110,WHITE);
delay(j*100);
}

for(i=0;i<=d;i++)

{
setfillstyle(1,RED); 
rectangle(315,105,415,205);
floodfill(320,110,RED);
delay(j*100); setfillstyle(1,2); 
rectangle(315,105,415,205);
floodfill(320,110,WHITE);
delay(j*100);
}

for(i=0;i<=;ei++)

{
setfillstyle(1,RED); 
rectangle(210,210,310,310);
floodfill(215,215,RED);
delay(j*100); setfillstyle(1,3); 
rectangle(210,210,310,310);
floodfill(215,215,WHITE);
delay(j*100);
}

for(i=0;i<=f;i++)

{
setfillstyle(1,RED); 
rectangle(315,210,415,310);
floodfill(320,215,RED);
delay(j*100); setfillstyle(1,6); 
rectangle(315,210,415,310);
floodfill(320,215,WHITE);
delay(j*100);
}

printf("\nEnter the value "); 
scanf("%d%d%d%d",&l,&m,&n,&o);
if(l==c+1&&m==d+1&&n==e+1&&o==f+1)
{
for(;k<=20;)

{
printf("\nWelcome to level %d",k);
delay(1000);
goto x;
}
}else
{
printf("\nGame over");
}
printf("\n%d%d%d%d",c+1,d+1,e+1,f+1);
getch();
}

void load()

{
int i=275,x=40,y=15,j,a; 
arc(274,270,90,270,10);
arc(274,270,90,270,9); 
arc(274,270,90,270,8); 
arc(375,270,270,90,8); 
arc(375,270,270,90,9); 
arc(375,270,270,90,10);
line(275,260,375,260);
line(275,261,375,261);
line(275,279,375,279);
line(275,280,375,280); 
setfillstyle(1,GREEN); 
circle(275,270,8);
floodfill(280,275,WHITE);

for(j=1;j<=100;j++)

{
gotoxy(x,y);
printf("%d%%",j); 
a=i++; 
circle(a,270,8);
delay(100);
}

clrscr();
}
