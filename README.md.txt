#include<reg51.h>
sbit A=P1^0;
sbit b=P2^0;
sbit C=P3^0;
unsigned char SA[]={0,0,0,0,1,1,1,1};
unsigned char SB[]={0,0,1,1,0,0,1,1};
unsigned char SC[]={0,1,0,1,0,1,0,1};
unsigned char A2[]={0x3f,0x06,0x5b,0x4f,0x66,0x6d,0x07,0x7f};
void delay(int i,j)
{
for(i;i>0;i--)
for(j=110;j>0;j--);
}
void main()
{
while(1)
{
int a;
for(a=0;a<8;a++);
C=SC[a];b=SB[a];C=SC[a];
{
P0=A2[a];
delay(10);
P0=0x00;
}
}
}
