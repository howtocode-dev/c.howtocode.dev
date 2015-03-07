#কন্ডিশনাল অপারেটর
Conditional Operator: একটা condition দিয়ে দুটি মান select করার একটা পদ্ধতি। এটি নিচের মতো করে লেখা হয়ঃ

Expression1? Expression2: Expression3

যেমনঃ

মনে করি i=5, তাহলে নিচের Conditional Operator টা দেখিঃ

Z=(i<8)?10:100;

এখানে Z এর জন্য Conditional Operator টা লেখা হয়েছে। এখানে লিখা হয়েছেঃ Z=(i<8)?10:100; অর্থাত যদি i এর মান 8 থেকে ছোট হয় তাহলে Z এর মান হবে 10। আর তা না হলে z এর মান হবে 100.

আমি নিচের প্রোগ্রামে সব কিছু বুঝানোর চেষ্টা করছিঃ

if-else statement এর পরিবর্তে Conditional Operator (?:) ব্যবহার করে সহজেই দুইটি statement অথবা valu এর মধ্যে তুলনা করে একটি মান নির্বাচিত করা যায়। Conditional Operator সি প্রোগ্রামিং এ নিচের মত করে লেখা হয়ঃ

condition ? first_expression : second_expression;

এখানে condition  হচ্ছে যে কোন একটা শর্ত। যা সত্য হলে   first_expression নির্বাচিত হবে। আর কন্ডিশন ভুল হলে second_expression।
নিচে ছোট্ট একটা প্রোগ্রাম। যা দিয়ে দুটি সংখ্যার মধ্যে বড়টা নির্বাচিত  করা হয়েছে।


```c
#include <stdio.h>
int main()
{
 int x, y , result;
 scanf("%d %d", &x , &y);
 result = (x>=y) ? x : y ;
 printf("max is %d", result);
 return 0;
}
```
একই প্রোগ্রাম, কন্ডিশন পরিবর্তন করে  দুটি সংখ্যার মধ্যে ছোটটা নির্বাচিত  করা হয়েছে।

```c
#include <stdio.h>
 
int main()
{
 int x, y , result;
 scanf("%d %d", &x , &y);
 result = (x<=y) ? x : y ;
 printf("min is %d", result);
 return 0;
}
```
যদিও একই কাজ if -else বা অন্য অনেক ভাবে করা যায়।