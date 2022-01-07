#include<stdio.h>
#include<stdlib.h>

int main()
{
int a,b;
scanf("%d%d",&a,&b);
int m[1000][1000],s1=0,s2=0;
for(int i=0;i<a;i++){
    for(int j=0;j<b;j++){
        scanf("%d",&m[i][j]);
    }
}
for(int k=0;k<b;k++){
for(int i=0;i<a;i++){
    for(int j=0;j<b;j++){
        if(j<=k){
            s1+=m[i][j];
        }
        if(j>k){
            s2+=m[i][j];
        }
        if(i==a-1 && j==b-1)
        {
            if(s1==s2){
                printf("YES");
            }
            else{
                s1=0;
                s2=0;
                }
        }
    }
}
printf("NO");
}