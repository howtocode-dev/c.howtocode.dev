#Assignment operator

Assignment operator: কোন মান বা Value কোন Identifier [ভ্যারিয়েবল] এর মধ্যে assign করা বা একটা মান রাখার জন্য জন্য assignment operator ব্যবহৃত হয়। C তে অনেক রকম Assignment operator রয়েছে। যেমনঃ

1)    = (Equal to)

2)    +=(Plas equal to)

3)    -=(Mainus equal to)

4)    *=(Product equal to)

5)    /=(Division equal to)

6)    %= (Mode equal to) etc

তবে সবছেয়ে ব্যবহৃত Assignment operator হচ্ছে = (Equal to)।  এটি নিচের from এ লিখা হয়।

Identifier=expression

এখানে Identifier বলতে সাধারনত চলক(variable) কে বুঝানো হয়। আর expression বলতে যে কোন মান যেমন constant বা variable ইত্যাদি কে বুঝানো হয়।

নিচে কিছু Assignment operator এর উদাহরন দেওয়া হলোঃ

X=5;
Y=10;
Pi=3.1416
Z=x+y+pi

এখানে প্রথম উদাহরনে 5 , x এর মধ্য assign হয়েছে। অর্থাৎ x এর মান এখন 5।  দ্বিতীয় উদাহরনে 10 , y এর মধ্য assign হয়েছে। অর্থাৎ y এর মান এখন 10. তৃতীয় উদাহরনে 3.1416 , pi এর মধ্য assign হয়েছে। অর্থাৎ pi এর মান এখন 3.1416. চতুর্থ উদাহরনে (x+y+pi ) , z এর মধ্য assign হয়েছে। অর্থাৎ z এর মান এখন (x+y+pi ) ।

আমরা এর আগেই  assignment operator ব্যবহার করে এসেছি।

আগের একটি প্রোগ্রামই দেখি, যেখানে আমরা আয়াতাকার  জমির আয়তন বের করেছি।

```c
#include <stdio.h>
 
int main()
{
 int volume;
 int length = 5;
 int width = 8;
 volume = length * width;
 printf("%d", volume);
 return 0;
}
```
যেখানে length নামক একটি ভ্যারিয়েবল এ আমরা একটি মান [5] রেখেছি। এবং width ভ্যারিয়েবলে রেখেছি 8.

+= (Plas equal to) Assignment operator:

এটা নিচের মতো করে লেখা হয়

Expression1 += Expression2;

যা (Expression1 = Expression1 + Expression2 ) এর সমান।

ব্যাখ্যাঃ মনে করি x=3 , y=5.

যদি লেখা হয়: x+=y তাহলে x এর মান হবে x=x+y অর্থাৎ x=8.

```c
#include <stdio.h>
 
int main()
{
 int x =3;
int y = 5;
x +=y;
 printf("%d", x);
 return 0;
}
```
উপরের প্রোগ্রামটা রান করিয়ে দেখলে আমরা আউটপুট পাবোঃ 8
নিচের প্রোগ্রামটা দেখিঃ
```c
#include <stdio.h>
 
int main()
{
 int x =3;
int y = 5;
x = x+y;
 printf("%d", x);
 return 0;
}
```
এ প্রোগ্রামও রান করিয়ে দেখলে আমরা আউটপুট পাবোঃ 8
আউটপুটে কোন পার্থ্যক্য নেই। কম কোড লেখার জন্য প্রায় সময়ই += অপারেটর ব্যবহার করা হয়। 

-= (Mainus equal to) Assignment operator

-= এর ক্ষেত্রে নিচের মতো করে লেখা হয়

Exprission1 -= Expression2;

যা (Expression1 = Expression1 – Expression2 ) এর সমান।

ব্যাখ্যাঃ মনে করি x=8 , y=5.

যদি লেখা হয়ঃ x-=y তাহলে x এর মান হবে x=x-y অর্থাৎ x=3.

```c
#include <stdio.h>
 
int main()
{
 int x =8;
int y = 5;
x -=y;
 printf("%d", x);
 return 0;
}
```
উপরের প্রোগ্রামটা রান করিয়ে দেখলে আমরা আউটপুট পাবোঃ 3
নিচের প্রোগ্রামটা দেখিঃ


```c
#include<stdio.h>
int main()
{
 int x =8;
int y = 5;
x = x-y;
 printf("%d", x);
 return 0;
}
```
এ প্রোগ্রামও রান করিয়ে দেখলে আমরা আউটপুট পাবোঃ 3
উপরের প্রোগ্রামের সাথে আউটপুটে কোন পার্থ্যক্য নেই।  += অপারেটর এর মতই কম কোড লেখার জন্য প্রায় সময় -= ব্যবহার করা হয়। 

একই ভাবে  *= এর মানে হচ্ছেঃ

Exprission1 *= Expression2;

যা (Expression1 = Expression1 * Expression2 ) এর সমান।

/= এর মানে হচ্ছেঃ

Expression1 /= Expression2;

যা (Expression1 = Expression1 / Expression2 ) এর সমান।

%= এর মানে হচ্ছেঃ

Expression1 %= Expression2;

যা (Expression1 = Expression1 % Expression2 ) এর সমান।