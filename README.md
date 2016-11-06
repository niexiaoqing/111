# include <stdio.h>
# include <windows.h>
# include <time.h>
double getPI1(double h){
 double l = 1.0/h;
 int i,j;
 double s = 0;
 for(i = 0; i <= h; i++){
  s += l*(4/((1+i*l*i*l)))/2+l*4/(1+((i+1)*l*(i+1)*l))/2;
 }
 return s;
}
int main()
{
long op,ed;
op=clock();
double PI;
PI=getPI1(1000000);
ed=clock();
printf("π=%.12f\n",PI);
printf("%ldms\n",ed-op);
return 0;
}
