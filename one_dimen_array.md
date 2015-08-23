###অ্যারে ডিক্লেয়ারেশন

সি তে অ্যারে ব্যবহার করার আগে সেগুলোকে ডিক্লেয়ার করে নিতে হয় সাধারণ ভ্যারিয়েবলের মতই। অ্যারে ডিক্লেয়ারেশনের সিনট্যাক্স হচ্ছে

```c
	dataType Array_Name [ size ];
```

এখানে `dataType` হচ্ছে অ্যারেটি কী ধরনের ডেটা রাখবে তার টাইপ। তারপরে অ্যারের নাম, এবং সবশেষে `size` হচ্ছে অ্যারেতে এলিমেন্টের সংখ্যা।


অ্যারে অ্যাকসেস করতে হলে অ্যারের ইনডেক্স নাম্বারটি নির্দিস্ট করে বলতে হয়। অ্যারের ইনডেক্সিং শুরু হয় জিরো বা শূণ্য থেকে। আসুন আমরা অ্যারে নিয়ে বেসিক একটি প্রোগ্রাম দেখি। এখানে আরা অ্যারে ডিক্লেয়ার করব, সেটিতে ভ্যালু রাখব, প্রিন্ট করব এবং কয়েকটি সাধারণ অপারেশন দেখব।


```c
#include<stdio.h>

int main(void)
{

int age[5] = {18, 30, 50, 47, 57}; //array declaration and assigning values

printf("%d", age[0]);  //Printing the first element
printf("\n%d", age[3]); //Printing the 4th element

age[2] = 80; //changing a value

printf("\n%d", age[2]); //printing the changed value

printf("\nEnter age of person 1 :");
scanf("%d", &age[0]); //using scanf to insert a value in the array
printf("The newly assigned age for person 1 is : %d", age[0]);

return 0;
}

```

এখানে আমরা একটি অ্যারে ডিক্লেয়ার করে সেটিতে পাঁচটি ভ্যালু অ্যাসাইন করলাম। এরপর প্রথম ভ্যালুটি প্রিনট করালাম `printf("%d", age[0]);` দিয়ে। `printf("%d", age[3]);` দিয়ে আমরা চতুর্থ ভ্যালুটি প্রিন্ট করেছি। এরপর আমরা তৃতীয় ভ্যালু যার ইনডেক্স `2` সেটিকে পাল্টিয়েছি এবং প্রিন্ট করেছি। তারপরে আমরা scanf ব্যবহার করে একটি ভ্যালু নিয়ে প্রথম ইনডেক্সে রেখেছি এবং সেটি প্রিন্ট করেছি।

অ্যারের ভ্যালুগুলোকে অ্যাকসেস করার জন্য `for` লুপ ব্যবহার করা একটি প্রচলিত প্র্যাকটিস। আমরা আরেকটি উদাহরণ দেখব যেখানে আমরা `for` লুপ ব্যবহার করে অ্যারে অ্যাকসেস করছি এবং কয়েকটি সংখ্যার গড় বের করছি।

```c
#include<stdio.h>

int main(void)
{

int expenses[5];
int i;
int sum = 0;
float average = 0;

printf("Enter your expenses for last 5 days: ");

for(i=0; i<=4; i++) {
scanf("%d", &expenses[i]); //assigning all the values
}

for (i=0; i<=4; i++) {
sum = sum + expenses[i];
}

average = sum/5;

printf("Your average expenses for last five days is : %f", average);

return 0;
}
```

এই প্রোগ্রামটিতে আমরা আমাদের গত পাঁচদিনের গড় ব্যয় বের করছি। আমরা `expenses` নামের একটি অ্যারে এখানে ডিক্লেয়ার করেছি এবং এরপর একটি `for` লুপ ব্যবহার করে `scanf()` দিয়ে আমরা ভ্যালুগুলো অ্যারেতে নিয়েছি। আবার আরেকটি `for` লুপ দিয়ে আমরা `sum` বের করেছি এবং তারপরে `average` বের করে প্রিন্ট করেছি। এখানে একটি বিষয় লক্ষ্যনীয় যে আমরা `for` লুপের ইনডেক্স `i` কে অ্যারের ইনডেক্স হিসেবে ব্যবহার করেছি `expenses[i]` দিয়ে।
