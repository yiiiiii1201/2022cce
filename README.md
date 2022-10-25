# 2022cce
## 2層迴圈-畫星星
```cpp
#include <stdio.h>

int main()
{
    for(int i=5;i>0;i--){
        for(int j=0;j<i;j++){
            printf("*");
        }
        printf("i:%d星星\n",i);
    }
}
```
## 等腰三角形畫星星
```cpp
#include <stdio.h>

int main()
{
    for(int i=1;i<=5;i++){
        int space=5-i,star=2*i-1;
        for(int k=0;k<space;k++) printf(" ");
        for(int k=0;k<star;k++) printf("*");
        printf("\n");
    }
}
```
## 最大公因數-暴力迴圈法
```cpp
#include <stdio.h>

int main()
{
    printf("請輸入2個整數,要約分: ");
    int a,b;
    scanf("%d%d",&a,&b);

    int ans;
    for(int i=1;i<=a;i++){
        if(a%i==0&&b%i==0){
            ans=i;
        }
    }
    printf("ans:%d可約分",ans);
}
```
## 最大公因數-輾轉相除法
```cpp
#include <stdio.h>

int main()
{
    int a,b,c;
    scanf("%d%d",&a,&b);
    while(1){
        c=a%b;
        printf("老大:%d 老二:%d 老三:%d\n",a,b,c);
        if(c==0) break;
        a=b;
        b=c;
    }
    printf("答案b:%d",b);
}
```

##質數判別
```cpp
#include <stdio.h>

int main()
{
    int n;
    scanf("%d",&n);

    int bad=0;
    for(int i=2;i<n;i++){
        if(n%i==0) bad=1;
    }
    if(bad==0) printf("%d 是質數",n);
    else printf("%d 不好,不是質數",n);
}
```

##很多質數
```cpp
#include <stdio.h>

int main()
{
	int a;
	scanf("%d",&a);

	for(int n=2;n<=a;n++){
		int bad=0;
		for(int i=2;i<n;i++){
			if(n%i==0) bad=1;
        }
		if(bad==0) printf("%d ",n);
	}
}
```

##實習講解、練習
##[for2] 以*輸出直角三角形
#include <stdio.h>

int main()
{
    int n;
    scanf("%d",&n);

    for(int i=1;i<=n;i++){
        for(int k=1;k<=n;k++) printf(" ");
        for(int k=1;k<=i;k++) printf("*");
        printf("\n");
    }
}

#include <stdio.h>

int main()
{
    int n;
    scanf("%d",&n);

    for(int i=1;i<=n;i++){
        for(int k=1;k<=n;k++){
            if(k<=n-i) printf(" ");
            else printf("*");
        }
        printf("\n");
    }
}
```

##[while2] 以*輸出直角三角形 
```cpp
#include <stdio.h>

int main()
{
    int n;
    scanf("%d,&n");
    
    int i=1;
    while(i<=n){
    
    	int k=1;
        while(k<=n){
        
        	if(k<=n-i) printf(" ");
            else printf("*");
            
            k++;
        }
        printf("\n");
        i++;
    }
}
```
## 相加
#include <stdio.h>

int main()
{
    printf("請輸入5個數字(要加起來): ");

    int n;
    int sum=0;
    for(int i=0;i<5;i++){
        scanf("%d",&n);
        sum+=n;
    }
    printf("總和是:%d",sum);

}

 
 
         
 
  
 
  
 
   
