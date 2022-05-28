# 百科园

## 选择题

### 6

> 共15题。

下面能正确进行字符串赋值操作的是( )

- [ ] `char s[5]={"ABCDE"};`
- [ ] `char *s; scanf("%s",s) ;`
- [x] `char *s ; s="ABCDE" ;`
- [ ] `char s[5]={'A','B','C','D','E'};`

已有函数max(a,b)，为了让函数指针变量p指向函数max，正确的赋值方法是(  )。

- [ ] `*p=max;`
- [ ] `p=max(a,b);`
- [x] `p=max;`
- [ ] `*p=max(a,b);`

若有定义:int (*p)[4];则标识符p(  )。

- [x] 是一个指针，它指向一个含有四个整型元素的一维数组
- [ ] 定义不合法
- [ ] 是一个指向整型变量的指针
- [ ] 是一个指针数组名

下面程序段的运行结果是（  ）。

```c
char a[ ]=”language” , *p ;
p=a ; 
while (*p!='u') { printf(“%c”,*p-32); p++ ; }
```

- [ ] langUAGE
- [ ] LANGUAGE
- [x] LANG
- [ ] language

若要对a进行自增运算，则a应具有下面说明(  )。

- [ ] `char (*a)[3]`
- [ ] `char *a[ ]={"12","ab"};`
- [ ] `int a[3][2];`
- [x] `int b[10], *a=b;`

设p1和p2是指向同一个字符串的指针变量，c为字符变量，则以下能正确执行并得到有意义的结果的赋值语句是(  )。

- [ ] `c=*p1+*p2;`
- [x] `p1=p2;`
- [ ] `c=*p1*(*p2);`
- [ ] `p2=c;`

若有说明：int *p1, *p2,m=5,n;以下均是正确赋值语句的选项是( )。

- [ ] `p1=&m; p2=&p1 ;`
- [ ] `p1=&m; *p1=*p2 ;`
- [ ] `p1=&m; p2=&n; *p1=*p2 ;`
- [x] `p1=&m; p2=p1 ;`

下面程序段的运行结果是( )。

```c
char *s=”abcde” ;
s+=2 ; printf(“%s”,s);
```

- [x] `cde`
- [ ] `字符'c'`
- [ ] `不确定`
- [ ] `字符'c'的地址`

下面判断正确的是（）。

- [ ] `char *a="china"; 等价于 char *a; *a="china" ;`
- [ ] `char c[4]="abc",d[4]="abc"; 等价于 char c[4]=d[4]="abc" ;`
- [x] `char *s="china"; 等价于 char *s; s="china" ;`
- [ ] `char str[10]={"china"}; 等价于 char str[10]; str[ ]={"china";}`

设有程序段:`char s[ ]="china"; char *p ; p=s ;`则下面叙述正确的是（）。

- [ ] `s和p完全相同`
- [ ] `s数组长度和p所指向的字符串长度相等`
- [ ] `数组s中的内容和指针变量p中的内容相等`
- [x] `*p与s[0]相等`

已有定义`int k=2;int *ptr1,*ptr2;`且ptr1和ptr2均已指向变量k，下面不能正确执行的赋值语句是( )

- [ ] `k=*ptr1*(*ptr2);`
- [ ] `k=*ptr1+*ptr2;`
- [ ] `ptr1=ptr2;`
- [x] `ptr2=k;`

若有说明：int *p,m=5,n;以下程序段正确的是( )

- [ ] `p=&n ;scanf("%d",&p);`
- [ ] `scanf("%d",&n); *p=n ;`

这个不正确属实离谱！

```c
#include <stdio.h>
int main()
{
    int *p,m=5,n;
    scanf("%d",&n);
    *p=n ;
    printf("%d",*p);
    return 0;
}
```

```
10

```

竟然没能成功输出！

- [ ] `p = &n ;scanf("%d",*p);`
- [x] `p = &n ; *p = m ;`

已有变量定义和函数调用语句：`int a=25;print_value(&a);`下面函数的输出结果是( )

```c
void print_value(int *x)
{ printf(“%d\n”,++*x); }
```

- [x] `26`
- [ ] `25`
- [ ] `24`
- [ ] `23`

变量的指针，其含义是指该变量的( )

- [ ] `名`
- [x] `地址`
- [ ] `一个标志`
- [ ] `值`







## 程序设计

### 6

#### 6.1

```c
/*请编写函数fun,其功能是:将两个两位数的正整数a、b合并形成一个整数放在c中。
合并的方式是:将a数的十位和个位依次放在c数的千位和十位上,b数的十位和个位依次放在c数的百位和个位上。
例如,当a=45,b=12,调用该项函数后,c=4152。 
注意:部分源程序给出如下。 
请勿改动main函数和其他函数中的任何内容,仅在函数fun的花括号中填入所编写的若干语句。
试题程序: */
#include <stdio.h>
#include <conio.h>
void fun(int a ,int b,long *c)
{
  /************Begin************/



  /************End***************/
}
int main()
{
  int  a,b,i;  
  long c;
  FILE *out,*in;
  printf("Input a ,b: ");
  scanf("%d%d",&a,&b);
  fun(a,b,&c);
  printf("The result is :%ld\n",c);
  /******************************/
  in=fopen("in20.dat","r");
  out=fopen("out20.dat","w");
  for(i=10;i<20;i++)
  {
   fscanf(in,"%d %d",&a,&b);
	fun(a,b,&c);
	fprintf(out,"%d\n",c);
  }
fclose(out);
fclose(in);
/******************************/
return 0;
}

```







#### 6.2

```c
/*请编一个函数fun(char *s),该函数的功能是把字符串中的内容逆置。
例如,字符串中原有的字符串为abcdefg,则调用该函数后,串中的内容为gfedcba。
注意:部分源程序给出如下。
请勿改动main函数和其他函数中的任何内容,仅在函数fun的花括号中填入所编写的若干语句。
试题程序:*/
#include <string.h>
#include <stdio.h>
#define N 81
void fun(char*s)
{
/************Begin*************/


/************End**************/
}
int main()
{
	 char a[N];
	 FILE *out,*in;
	 printf("Enter a string:");
	 gets(a);
	 printf("The  original string is:");
	 puts(a);
	 fun(a);
	 printf("\n");
	 printf("The string after modified:");
	 puts(a);
	 strcpy(a,"Hello World! This is a first C program!");
	 fun(a);
	 /******************************/
      in=fopen("in17.dat","r");
      fgets(a,81,in);
	 out=fopen("out17.dat","w");
        fun(a);
	 fprintf(out,"%s",a);
	 fclose(out);
       fclose(in);
	 /******************************/
      return 0;
}

```







#### 6.3

```c
/*请编写函数fun,该函数的功能是:判断字符串是否为回文,若是则函数返回1,主函数中输出"YES",否则返回0,主函数中输出"NO"。
回文是指顺读和倒读都一样的字符串。例如,字符串LEVEL是回文,而字符串123312就不是回文。
注意:部分源程序给出如下。请勿改动main函数和其他函数中的任何内容,仅在函数fun的花括号中填入所编写的若干语句。
试题程序:*/
#include <stdio.h>
#define N 80
int fun(char str[])
{
    /***************Begin************/


    /*************** End ************/
}
int main()
{
	 char s[N];
	 FILE *out,*in;
         char test[][80]={"1234321","123421","123321","abcdCBA"};
	 int i;
	 printf("Enter a string : ");
	 gets(s);
	 printf("\n\n");
	 puts(s);
	 if(fun(s))
		printf("YES\n");
	 else
		printf("NO\n"); 
	 /************************************/
    in=fopen("in12.dat","r");
    for(i=0;i<4;i++)
    fscanf(in,"%s",test[i]);
	 out=fopen("out12.dat","w");
	 for(i=0;i<4;i++)
	 	if(fun(test[i]))
			fprintf(out,"YES\n");
		else
			fprintf(out,"NO\n");
    fclose(in);
	 fclose(out);
	 /************************************/
  return 0;
}

```







#### 6.4

```c
/*请编写函数fun,该函数的功能是:统计一行字符串中单词的个数,作为函数值返回。
一行字符串在主函数中输入,规定所有单词由小写字母组成,单词之间有若干个空格隔开,一行的开始没有空格。 
注意:部分源程序给出如下。 
请勿改动main函数和其他函数中的任何内容,仅在函数fun的花括号中填入所编写的若干语句。 
试题程序:*/
#include<string.h>
#include<stdio.h>
#define N 80
int fun(char *s)
{
 /************Begin*************/



/*************End*************/
}
int main()
{ 
  FILE *wf,*in;
  char line[N]; 
  int num=0;
  printf("Enter a string:\n "); 
  gets(line);
  num=fun(line);
  printf("The number of word is:%d\n\n ",num);
/******************************/
 in=fopen("in19.dat","r");
  wf=fopen("out19.dat","w");
  fgets(line,81,in);
  fprintf(wf,"%d",fun(line));
  fclose(wf);
  fclose(in);
/*****************************/
  return 0;
}
```





#### 6.5

```c
/*假定输入的字符串中只包含字母和*号。请编写函数fun,它的功能是:将字符串中的前导*号全部删除,中间和后面的*号不删除。
例如,若字符串中的内容为****A*BC*DEF*G*******,删除后,字符串中的内容则应当是A*BC*DEF*G*******。
注意:部分源程序给出如下。 
请勿改动main函数和其他函数中的任何内容,仅在函数fun的花括号中填入所编写的若干语句。 
试题程序: */
#include <stdio.h>
void  fun  (char *a)
{
/************Begin**************/



/************End*************/
}
int main()
{
  FILE *wf,*in;
  int i;
  char s[81],t[81]="****A*BC*DEF*G*******";
  printf("Enter a string :\n");
  gets(s);
  fun(s);
  printf("The string after deleted:\n");puts(s);
/******************************/
  in=fopen("in18.dat","r");
  wf=fopen("out18.dat","w");
  for(i=0;i<8;i++)
  {
	  fscanf(in,"%s",t);
	  fun(t);
      fprintf(wf,"%s\n",t);
  }
  fclose(in);
  fclose(wf);
/*****************************/
 return 0;
}
```



#### 6.6

```c
/*假定输入的字符串中只包含字母和*号。请编写函数fun,它的功能是:除了字符串前导的*号之外,将串中其他*号全部删除。
在编写函数时,不得使用C语言提供的字符串函数。 
例如,若字符串中的内容为****A*BC*DEF*G*******,删除后,字符串中的内容则应当是****ABCDEFG。 
注意:部分源程序给出如下。 
请勿改动main函数和其他函数中的任何内容,仅在函数fun的花括号中填入所编写的若干语句。 
试题程序: */
#include <string.h>
#include <stdio.h>
void  fun  (char *a)
{
/************Begin*************/



/************End**************/
}
int main()
{
  char s[81];
  FILE *in,*out;
  int i;
  printf("Enter a string :\n");
  gets(s);
  fun(s);
  printf("The string after deleted:\n");
  puts(s);
  /******************************/
  in=fopen("in21.dat","r");
  out=fopen("out21.dat","w");
  for(i=0;i<8;i++)
  {
	  fscanf(in,"%s",s);
	  fun(s);
      fprintf(out,"%s\n",s);
  }
  fclose(in);
  fclose(out);
  /******************************/
  return 0;
}

```





## 程序改错

### 6

#### 6.1

```c
/*假定输入的字符串中只包含字母和*号。函数fun的功能是:将字符串中的前导*号全部删除,中间和后面的*号不删除。
例如,若字符串中的内容为****A*BC*DEF*G*******,删除后,字符串中的内容则应当是A*BC*DEF*G*******。
注意:不得增行或删行,也不得更改程序的结构。
试题程序:
*/
#include <stdio.h>
#include<stdlib.h>
/**********ERROR**********/
void  fun(char *a);
{
    char *p=a;
/**********ERROR**********/
     while(*p!='*')
        p++; 
/**********ERROR**********/
    for(;*p!='\0';p++)
        *a=*p;
/**********ERROR**********/
    *a="\0"; 
}
int main()
{
	char s[81];
	printf("Enter a string :\n");
	gets(s);
/**********ERROR**********/
	fun(&s[80]);
	printf("The string after deleted:\n");
	puts(s);
       system("pause");
	return 0;
}

```

```c
【改错1】	错误
【学生答案】
void  fun(char *a);
【参考答案】
void  fun(char *a)
void  fun(char a[])

==============================
【改错2】	错误
【学生答案】
while(*p!='*')
【参考答案】
while(*p=='*')
*p=='*'
'*'==*p

==============================
【改错3】	错误
【学生答案】
for(;*p!='\0';p++)
【参考答案】
for(;*p!='\0';p++,a++)
for(;*p!='\0';a++,p++)
a++,p++
p++,a++
++a,++p
++p,++a
a=a+1,p++
p++,a=a+1
p++,a+=1
a+=1,p++

==============================
【改错4】	错误
【学生答案】
*a="\0"; 
【参考答案】
*a=0;
*a='\0';

==============================
【改错5】	错误
【学生答案】
fun(&s[80]);
【参考答案】
fun(s);
fun(&s[0]);

==============================

```



#### 6.2

```c
/*下列给定程序中,函数fun的功能是:计算s所指字符串中含有t所指字符串的数目,并作为函数值返回。 
请改正函数fun中的错误或在横线处填上适当的内容并把横线删除,使它能得出正确的结果。
注意:不要改动main函数,不得增行或删行,也不得更改程序的结构。
试题程序:*/
#include  <stdlib.h>
#include  <string.h>
#include  <stdio.h>
#define N 80
int fun(char *s,char *t)
{ int n;
  char *p, *r;
  n=0;
  p=&s[0];
/**********ERROR**********/
  *r=t;
  while(*p)
  { 
	if(*r==*p)
	{
		r++;
		if(*r=='\0')
		{	
			n++;
/**********ERROR**********/
			t=r;
		}
	}
  	p++;
  }
  return n;
}
int main()
{char a[N],b[N]; int m;
printf("\nPlease enter string a: ");
gets(a);
 printf("\nPlease enter substring b: ");
gets(b);
/**********ERROR**********/
 m=fun(a[N],b[N]);
 m=printf("\nThe result is :m=%d\n",m);
return 0;
}

```



```c
【改错1】	错误
【学生答案】
*r=t;
【参考答案】
r=t;

==============================
【改错2】	错误
【学生答案】
t=r;
【参考答案】
r=t;
r=&t[0];

==============================
【改错3】	错误
【学生答案】
m=fun(a[N],b[N]);
【参考答案】
m=fun(a,b);

==============================

```



#### 6.3

```c
/*下列给定程序中函数fun的功能是:先将在字符串s中的字符按逆序存放到t串中,然后把s中的字符按正序连接到t串的后面。
例如,当s中的字符串为ABCDE时,则t中的字符串应为EDCBAABCDE。
请改正程序中的错误,使它能得出正确的结果。
注意:不要改动main函数,不得增行或删行,也不得更改程序的结构。
试题程序: */
#include  <stdlib.h>
#include  <stdio.h>
#include  <string.h>
void fun (char *s, char *t )
{
  int i,s1;
  s1=strlen(s);    
  for (i=0;i<s1;i++)
/**********ERROR**********/
      t[i]=s[s1-1];    
  for (i=0;i<s1;i++)
      t[s1+i]=s[i];
/**********ERROR**********/
  t[2*s1]='0';
}
int main()
{char s[100], t[100];
  printf("\nPlease enter string s: "); 
  scanf("%s",s);
/**********ERROR**********/
  fun(s[100],t[100]);
  printf ("The result is: %s\n",t);
return 0;
}

```



```c
【改错1】	错误
【学生答案】
t[i]=s[s1-1];    
【参考答案】
t[i]=s[s1-1-i];
t[i]=s[s1-i-1];

==============================
【改错2】	错误
【学生答案】
t[2*s1]='0';
【参考答案】
t[2*s1]='\0';
t[2*s1]=0;

==============================
【改错3】	错误
【学生答案】
fun(s[100],t[100]);
【参考答案】
fun(s,t);

==============================

```



#### 6.4

```c
/*下列给定程序中函数fun的功能是:将长整型数中每一位上为奇数的数依次取出,构成一个新数放在t中。高位仍在高位,低位仍在低位。
例如当s中的数为87653142时,t中的数为7531。 请改正函数fun中的错误,使它能得出正确的结果。 
注意:不要改动main函数,不得增行或删行,也不得更改程序的结构。  试题程序:*/
#include  <stdlib.h>
#include  <stdio.h>
void fun(long s,long *t)
{int d;
 long s1=1;
/**********ERROR**********/
 t=0;
 while(s>0)
    { d=s%10;
/**********ERROR**********/
      if(d%2==0)
        {*t=d*s1+*t;
         s1*=10;
        }
    s/=10;
    }
}  
int main()
{
long s, t;
printf("\nPlease enter s: "); scanf("%ld",&s);
/**********ERROR**********/
 fun(s,t);
 printf("The result is :%ld\n",t);
return 0;
}

```



```c
【改错1】	错误
【学生答案】
t=0;
【参考答案】
*t
*t=0;

==============================
【改错2】	错误
【学生答案】
if(d%2==0)
【参考答案】
if(d%2!=0)
if(d%2)
if(d%2==1)

==============================
【改错3】	错误
【学生答案】
fun(s,t);
【参考答案】
fun(s,&t);

==============================

```



#### 6.5

```c
/*下列给定程序中,函数fun的功能是:在字符串str中找出ASCII码值最大的字符,将其放在第一个位置上,
并将该字符前的原字符向后顺序移动。例如,调用fun函数之前给字符串输入ABCDeFGH,调用后字符串中的内容为eABCDFGH。
请改正程序中的错误,使它能得出正确的结果。
注意:不要改动main函数,不得增行或删行,也不得更改程序的结构。
试题程序: */
#include <stdio.h>
/**********ERROR**********/
fun(char *p)
{ char max, *q;int i=0;
  max=p[i];
  while (p[i]!=0)
       {if (max<=p[i])
          { 
/**********ERROR**********/
           p = q +i;max=p[i];
          }
        i++;
       }
/**********ERROR**********/
  while(q<p)
      {*q=*(q-1);
        q--;
       }
  p[0]=max;
}
int main()
{char str[80];
  printf("Enter a string: "); gets(str);
  printf("\nThe original string: "); 
puts(str);
  fun(str);
  printf("\nThe string after moving: ");
puts(str); printf("\n\n");
return 0;
}

```



```c
【改错1】	错误
【学生答案】
fun(char *p)
【参考答案】
void fun(char *p)

==============================
【改错2】	错误
【学生答案】
p = q +i;max=p[i];
【参考答案】
q=p+i;
q=i+p;

==============================
【改错3】	错误
【学生答案】
while(q<p)
【参考答案】
while(q>p)
while(p<q)

==============================

```



#### 6.6

```c
/*下列给定程序中,函数fun的功能是:在字符串str中找出ASCII码值最大的字符,将其放在第一个位置上,并将该字符前的原字符向后顺序移动。
例如,调用fun函数之前给字符串输入ABCDeFGH,调用后字符串中的内容为eABCDFGH。 
请改正程序中的错误,使它能得出正确的结果。 
注意:不要改动main函数,不得增行或删行,也不得更改程序的结构。 
试题程序: */
#include <stdio.h>
/**********ERROR**********/
int fun(char *p)
{ 
char max, *q;
int i=0;
  max=p[i];
  while (p[i]!=0)
       {if (max<=p[i])
          { 
/**********ERROR**********/
           p = q +i;
max=p[i];
          }
        i++;
       }
/**********ERROR**********/
  while(q<p)
      {*q=*(q-1);
        q--;
       }
  p[0]=max;
}
int main()
{
char str[80];
  printf("Enter a string: "); 
gets(str);
  printf("\nThe original string: "); 
puts(str);
  fun(str);
  printf("\nThe string after moving: ");
puts(str); 
printf("\n\n");
return 0;
}

```



```c
【改错1】	错误
【学生答案】
int fun(char *p)
【参考答案】
void fun(char *p)

==============================
【改错2】	错误
【学生答案】
p = q +i;
【参考答案】
q=p+i;
q=i+p;

==============================
【改错3】	错误
【学生答案】
while(q<p)
【参考答案】
q>p
p<q

==============================

```





## 程序填空

### 6

#### 6.1

```c
/*给定程序的功能是:分别统计字符串中大写字母和小写字母的个数。 
例如,给字符串ss输入:AaaaBBb123CCccccd,则输出结果应为:upper=5,lower=9。
注意:部分源程序给出如下。
请勿改动函数中的其他内容,仅在横线上填入所编写的若干表达式或语句。
试题程序: */
#include <stdlib.h>
#include <stdio.h>
void fun(char *s,int *a,int *b)
{
	 while(*s)
	 {
		if(*s>='A' && *s<='Z')
/**********FILL**********/
		   [1]    ;
		if(*s>='a' && *s<='z')
/**********FILL**********/
		【2】     ;
	 	s++;
	 }
}

int main()
{
	 char s[100];
	 int upper=0,lower=0;
	 printf("\nPlease a string: ");
	 gets(s);
	 fun(s,&upper,&lower);
/**********FILL**********/
	 printf("\n upper=%d lower=%d\n",【3】     );
return 0;
} 

```



```c
【空 1 】	错误
【学生答案】
[1]    ;
【参考答案】
(*a)++
++(*a)
*a+=1
*a=*a+1

============================================================
【空 2 】	错误
【学生答案】
?2?     ;
【参考答案】
(*b)++
++(*b)
*b+=1
*b=*b+1

============================================================
【空 3 】	错误
【学生答案】
printf("\n upper=%d lower=%d\n",?3?     );
【参考答案】
upper,lower

============================================================

```





#### 6.2

```c
/*请补充main函数,该函数的功能是:从键盘输入两个字符串并分别保存在字符数组str1和str2中,
用字符串str2替换字符串str1前面的所有字符。注意:str2的长度不大于str1,否则需要重新输入。
例如,如果输入str1="abced",str2="fk",则输出"fkced"。 
注意:部分源程序给出如下。 
请勿改动main函数和其他函数中的任何内容,仅在main函数的横线上填入所编写的若干表达式或语句。
试题程序:*/
#include <stdlib.h>
#include<stdio.h>
#include <string.h>
int main()
{
	 char str1[81],str2[81];
	 char *p1=str1,*p2=str2;
	 do
	 {
		printf(" Input str1 \n");
		gets(str1);
		printf(" Input str2 \n");
		gets(str2);
/**********FILL**********/
	 }while(   【1】   );
/**********FILL**********/
	 while(   【2】   )
		*p1++=*p2++;
	 printf(" Display str1 \n");
/**********FILL**********/
	 puts(   【3】   );
return 0;
} 

```



```c
【空 1 】	错误
【学生答案】
}while(   ?1?   );
【参考答案】
strlen(str1)<strlen(str2)
strlen(str2)>strlen(str1)

============================================================
【空 2 】	错误
【学生答案】
while(   ?2?   )
【参考答案】
*p2
*p2!=0

============================================================
【空 3 】	错误
【学生答案】
puts(   ?3?   );
【参考答案】
str1

============================================================

```



#### 6.3

```c
/*给定程序中,函数fun的功能是:在形参s所指字符串中的每个数字字符之后插入一个*号。
例如,形参s所指的字符串为:def35adh3kjsdf7。执行结果为:def3*5*adh3*kjsdf7*。
注意:部分源程序给出如下。
请勿改动main函数和其他函数中的任何内容,仅在函数fun的横线上填入所编写的若干表达式或语句。
试题程序:*/
#include <stdio.h>
void fun(char *s )
{
	 int i,j,n;
	 for(i=0;s[i]!='\0';i++)
/**********FILL**********/
	 if(s[i]>='0'   [1]  s[i]<='9')
	{
		n=0;
/**********FILL**********/
		while(s[i+1+n]!=  [2]  )
			n++;
		for(j=i+n+1;j>i;j--)
/**********FILL**********/
		s[j+1]=   [3]    ;
		s[j+1]='*';
			i=i+1;
		}
}
int main()
{
	char s[60]="ba3a54cd23a";
	printf("\n the original string is: %s\n",s);
	fun(s);
	printf("\nthe result is: %s\n",s);
return 0;
}

```



```c
【空 1 】	错误
【学生答案】
if(s[i]>='0'   [1]  s[i]<='9')
【参考答案】
&&

============================================================
【空 2 】	错误
【学生答案】
while(s[i+1+n]!=  [2]  )
【参考答案】
0
'\0'

============================================================
【空 3 】	错误
【学生答案】
s[j+1]=   [3]    ;
【参考答案】
s[j]
*(s+j)

============================================================

```





#### 6.4

```c
/*请补充函数fun,该函数的功能是:在字符串的最前端加入n个*号,形成新串,并且覆盖。注意:字符串的长度最长允许为79。
注意:部分源程序给出如下。请勿改动main函数和其他函数中的任何内容,仅在函数fun的横线上填入所编若干表达式或语句。
试题程序: */
#include  <stdlib.h>
#include  <stdio.h>
#include  <string.h>
void fun(char s[],int n)  
{
 char a[80],*p;
 int i;
/**********FILL**********/
 p=【1】;   
 for(i=0;i<n;i++)  a[i]= '*';
 do 
{
/**********FILL**********/
a[i]=【2】;
    i++;
/**********FILL**********/
 }while(【3】);
 a[i]=0;
 strcpy(s,a);
}
int main()
{
int n;char s[80];
printf("\nEnter a string: ");gets(s);
 printf("\nThe string:%s\n",s);
 printf("\nEnter n (number of*):");
 scanf("%d",&n);
 fun(s,n);
 printf("\nThe string after inster:%s\n",s);
return 0;
}

```



```c
【空 1 】	错误
【学生答案】
p=?1?;   
【参考答案】
p=s;
p=&s[0];

============================================================
【空 2 】	错误
【学生答案】
a[i]=?2?;
【参考答案】
a[i]=*p++;
a[i]=*(p++);

============================================================
【空 3 】	错误
【学生答案】
}while(?3?);
【参考答案】
*p!=0
*p!='\0'

============================================================

```



#### 6.5

```c
/*请补充main函数,该函数的功能是:从键盘输入若干字符放到一个字符数组中,当按回车键时结束输入,
最后输出这个字符数组中的所有字符。
注意:部分源程序给出如下。
请勿改动main函数和其他函数中的任何内容,仅在main函数的横线上填入所编写的若干表达式或语句。
试题程序:*/
#include <stdlib.h>
#include <stdio.h>
int main()
{
	 int i=0;
	 char s[81];
	 char *p=s;
	 printf(" Input a string \n");
	 for(i=0;i<80;i++)
	 {
		s[i]=getchar();
		if(s[i]=='\n')
/**********FILL**********/
			【1】   ;
	 }
/**********FILL**********/
	 s[i]=   【2】   ;
	 printf(" display the string \n");
	 while(*p)
/**********FILL**********/
		putchar(   【3】   );
return 0;
}

```



```c
【空 1 】	错误
【学生答案】
?1?   ;
【参考答案】
break

============================================================
【空 2 】	错误
【学生答案】
s[i]=   ?2?   ;
【参考答案】
0
'\0'

============================================================
【空 3 】	错误
【学生答案】
putchar(   ?3?   );
【参考答案】
*p++
*(p++)

============================================================

```

































