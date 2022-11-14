- 👋 Hi, I’m @zwt36823522
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
ghgfhgfghfh
<!---
zwt36823522/zwt36823522 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
dfgfd


打开APP



weixin_39878247
关注
c 语言游戏代码大全,给我提供个小游戏的C 语言代码 转载
2021-05-17 10:42:24

weixin_39878247 

码龄5年

关注
满意答案



fendadoris

2013.08.16



采纳率：50%    等级：9

已帮助：264人

2L你给的什么呀，明明是加密算法调用我给你一个贪吃蛇的 C# #define N 200/*定义全局常量*/

#define m 25

#include

#include

#include

#include

#define LEFT 0x4b00

#define RIGHT 0x4d00

#define DOWN 0x5000

#define UP 0x4800

#define Esc 0x011b

int i,j,key,k;

struct Food/*构造食物结构体*/

{

int x;

int y;

int yes;

}food;

struct Goods/*构造宝贝结构体*/

{

int x;

int y;

int yes;

}goods;

struct Block/*构造障碍物结构体*/

{

int x[m];

int y[m];

int yes;

}block;

struct Snake{/*构造蛇结构体*/

int x[N];

int y[N];

int node;

int direction;

int life;

}snake;

struct Game/*构建游戏级别参数体*/

{

int score;

int level;

int speed;

}game;

/*定义函数*/

void init(void);/*定义图形驱动*/

void close(void);/*定义关闭函数*/

void drawk(void);/*定义界面函数*/

void gameover(void);/*定义游戏结束函数*/

void gameplay(void);/*定义游戏主函数*/

void prscore(void);/*定义得分函数*/

void main(void){/*主函数体，调用以下四个函数*/

init();

setbkcolor(7);

drawk();

gameplay();

close();

}

void init(void){/*构建图形驱动函数*/

int gd=DETECT,gm;

initgraph(&gd,&gm,"");

cleardevice();

}

void drawk(void){/*构建游戏界面函数*/

/*setbkcolor(LIGHTGREEN);*/

char str3[50];

setfillstyle(SOLID_FILL,BLUE);/*条型边框,显示版本信息*/

bar3d(48,9,610,38,1,45);

setcolor(YELLOW);/*版本信息*/

sprintf(str3,"Version:5.01,Powerwing Studio");

outtextxy(330,20,str3);

setfillstyle(LTSLASH_FILL,YELLOW);/*设定墙边的填充形式*/

bar3d(48,48,58,462,0,0);/*设定墙边*/

bar3d(48,39,611,48,0,0);

bar3d(48,452,611,462,0,0);

bar3d(602,39,611,462,0,0);

}

void gameplay(void){/*构建游戏主函数*/

/*初始化游戏角色*/

randomize();/*随机数发生器*/

goods.yes=1;

block.yes=1;

food.yes=1;/*场景中需建立新的食物*/

snake.life=1;/*初始化蛇生命值*/

snake.direction=1;/*蛇起始的移动方向定义为向右*/

snake.x[0]=100;snake.y[0]=100;/*蛇头的位置坐标初始化*/

snake.x[1]=110;snake.y[1]=100;
