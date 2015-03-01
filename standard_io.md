#4.1. স্ট্যান্ডার্ড ইনপুট এবং আউটপুট
## getchar & putchar
এতক্ষন পর্যন্ত আমরা একটি ডেটা শুধু আউটপুট দিয়েছি। কিন্তু আমাদের প্রোগ্রামে আমরা শুধু কিছু মান আউটপুটই নিব না, ব্যবহারকারী থেকে কিছু ইনপুটও নিতে হবে। ইনপুট এবং আউটপুটের জন্য আজকে দুটি Function নিয়ে আলোচনা করব। একটা হচ্ছে “getchar” আরেকটি হচ্ছে “putchar” Function.

getchar Function: getchar Function দ্বারা single character কম্পিউটারে input নেওয়া হয়। এটি একটি C library Function. এটি সাধারনত নিছের মত করে লিখা হয়।

character variable =getchar( );

getchar Function হচ্ছে স্টান্ডার্ড C I/O library এর একটি অংশ। এটি ইনপুট ডিভাইস যেমন Keyboard থেকে একটি সিঙ্গেল Character দেয়।   প্রোগ্রামের মঝে এটি নিচের মত করে লিখা হয়ঃ

char x;

x= getchar();

এখানে char x; দ্বারা বুঝানো হয়েছে যে এটি একটি character type Variable. পরবর্তিতে x= getchar(); দ্বারা x এর মান ইনপুট ডিভাইস [ কীবোর্ড ] হতে নিবে।

```c

#include <stdio.h>

int main()
{
char x;
printf("Enter a character: ");
 x= getchar();
 printf("Your entered: %c", x);
 return 0;
}

```

উপরের প্রোগ্রামটা রান করুন এবং কীবোর্ড হতে একটি বর্ণ টাইপ করে এন্টারকী প্রেস করুন। এটি আপনি যা ইনপুট দিয়েছেন তাই প্রিন্ট করবে।

putchar Function: putchar Function দ্বারা single character কম্পিউটারে দেখানোর জন্য ব্যবহার করা হয়।   এটি getchar Function অনুরুপ।এটি সাধারনত নিছের মত করে লিখা হয়।

putchar(character variable );

এটি ও স্টান্ডার্ড  I/O library এর একটি অংশ।  প্রোগ্রামের মঝে এটি নিচের মত করে লিখা হয়ঃ

char x;

putchar(x);

getchar Function  এর মত এখানে char x; দ্বারা বুঝানো হয়েছে যে এটি একটি character type Variable. পরবর্তিতে putchar(x); দ্বারা x এর মান আউটপুট ডিভাইসে দেখাবে।

```c

#include <stdio.h>

int main()
{
 char x;
 x= getchar();
 putchar(x);
 return 0;
}

```

উপরের প্রোগ্রামে একটি character variable  x নিয়েছি। এখন প্রোগ্রামটি রান করার পর আপনি যাই ইনপুট দিবেন,  putchar Function দ্বারা আপনাকে দেখাবে।

 

ছোট অক্ষরকে বড় অক্ষরে পরিনত করাঃ


```c

#include <stdio.h>

int main()
{
 char x;
 x= getchar();
 putchar(toupper(x));
 return 0;
}

```

এ প্রোগ্রাম এ যে Character ই input হিসেবে নিবে তার Uppercase মানে বড় হাতের অক্ষর Output দিবে। আর বড় হতের দিলে ও বড় হাতের অক্ষর Output দিবে। তবে সংখা দিলে তাই Output দিবে।

এখানে আমরা toupper() নামক লাইব্রেরী ফাংশং ব্যবহার করেছি। নাম থেকেই তো এর কাজ বুঝা যায় তাই না?

বড় অক্ষরকে ছোট অক্ষরে পরিনত করাঃ

```c

#include <stdio.h>

int main()
{
char x;
x= getchar();
putchar(tolower(x));
return 0;
}

```

এ প্রোগ্রাম এ যে Character ই input হিসেবে নিবে তার Lowercase মানে ছোট হাতের অক্ষর Output দিবে। আর ছোট হতের দিলে  তাই Output দিবে।

##scanf & printf

আমরা এর আগে আমরা একটি মাত্র  character কম্পিউটারে কিভাবে getchar এর সাহায্যে input নেওয়া যায় তা দেখছি। এবার আমরা single character, numerical values এবং string কিভাবে কম্পিউটারে input নিব তা দেখবো। single character, numerical values. এবং string যেকোন মান কম্পিউটারে নেওয়ার জন্য “scanf” function ব্যবহার করা হয়। আবার putchar এর মত কোন মান পর্দায় দেখানোর জন্য “printf” function ব্যবহার করি যা আমরা এর আগেই ব্যবহার করা শুরু করেছি। putchar দিয়ে একটি মাত্র character কম্পিউটারে Output দেখানো যেত, কিন্তু “printf” function দ্বারা একদিক ডাটা যেমন single character, numerical values. এবং string ইত্যাদির যেকোন মান কম্পিউটারে Output দেখানো যায়।

“scanf” function ব্যবহারের নিয়মঃ

Scanf(control string, argument1, argument2,……..argumentn);

এখানে control string দ্বারা কোন ধরনের Data input নিব তার ফরমেট বুঝায়। আর argument দ্বারা Data কম্পিউটারে কোথায়(memory address এর কোন জাগায়) সংরক্ষন হবে তা বুঝায়।

যেমন একটি প্রোগ্রামে নিন্মোক্ত Scanf statement টি রয়েছেঃ

char name;

scanf(“%c”,&name);

এখানে name নামে একটি variable নেওয়া হয়েছে। তার পর আমরা এখন ইনপুট ডিভাইস থেকে এ চলকের মান  কম্পিউটারে নিব। এ জন্য Scanf(“%c”,&name); statement দিয়ে তা নেওয়া হয়েছে।

এখানে control string হচ্ছে c। প্রতিটি control string একটি % চিহ্ন দিয়ে শুরু করতে হয়। তাই এখানে control stringটি %c দ্বারা লিখা হয়েছে। এখানে c দ্বারা বুঝানো হয় যে Data item একটি single character। এরকম আরো অনেক গুলো control string রয়েছে। নিছে এর একটি তালিকা দেওয়া হল।

 | Code | Meaning |
| -- | -- |
| %a | Input হিসেবে Floating-point  Data item  নিতে পারবে। |
| %c | Input হিসেবে একটি মাত্র character Data item নিতে পারবে। |
|%d | Input হিসেবে Decimal integer Data item নিতে পারবে। |
|%e | Input হিসেবে Floating-point  Data item  নিতে পারবে।|
| %f | Input হিসেবে Floating-point  Data item  নিতে পারবে। |
| %g | Input হিসেবে Floating-point  Data item নিতে পারবে। |
|%i| Input হিসেবে Decimal, Hexadecimal or Octal Integer Data item  নিতে পারবে। |
| %o | Input হিসেবে Octal Integer Data item  নিতে পারবে। |
| %p | Input হিসেবে Pointer Data item নিতে পারবে।( Pointer সম্পর্কে পরে আলোচনা করা হবে)। |
| %s | Input হিসেবে String   Data item নিতে পারবে। |
| %u | Input হিসেবে Unsigned decimal Data item নিতে পারবে।
| %x | Input হিসেবে Hexadecimal Data item নিতে পারবেে।|


control string কে কেউ কেউ আবার Placeholder ও বলে থাকে। 

“printf” function ব্যবহারের নিয়মঃ

printf(control string, argument1, argument2,……..argumentn);

এখানে control string দ্বারা কোন ধরনের Data Output দিবে তার ফরমেট বুঝায়। আর argument দ্বারা প্রতিটি Output Data প্রকাশ করে। এখানে কিন্তু “scanf” function এর মত memory address প্রকাশ করে না।

যেমন একটি প্রোগ্রামে নিন্মোক্ত “printf”  statement টি রয়েছেঃ

char name;

printf(“%c”, name);

এখানে name নামে একটি Character variable নেওয়া হয়েছে। এখন মনে করি nameএর মান কম্পিউটারে আছে আমরা তার Output বের করবো।তাই printf(“%c”, name); দ্বারা তা Output ডিভাইসে প্রকাশ করে। এখানে ও control string হচ্ছে c।scanf এর মর printf এ ও প্রতিটি control string একটি % চিহ্ন দিয়ে শুরু করতে হয়। তাই এখানে control stringটি %c দ্বারা লিখা হয়েছে। এখানে c দ্বারা বুঝানো হয় যে Data item একটি single character। scanf ও printf এর control string একই। তবে scanf এর control string দ্বারা কি ধরনের মান ইনপুট নিবে তা বুঝায়, আর printf এর control string দ্বারা কিধরনের মান আউটপুট দিবে তা বুঝায়। নিচে printf এর control string গুলো দেওয়া হল।

|Code | Meaning |
| -- | -- |
| %a | এটি ব্যবহার করলে Floating-point  Data item  আউটপুট দিবে। |
| %c | এটি ব্যবহার করলে একটি মাত্র character Data item আউটপুট দিবে। |
| %d | এটি ব্যবহার করলে Decimal integer Data item আউটপুট দিবে। |
| %e | এটি ব্যবহার করলে Floating-point  Data item  আউটপুট দিবে। |
| %f | এটি ব্যবহার করলে Floating-point  Data item  আউটপুট দিবে। |
| %g | এটি ব্যবহার করলে Floating-point  Data item আউটপুট দিবে। |
| %i | এটি ব্যবহার করলে Decimal, Hexadecimal or Octal Integer Data item আউটপুট দিবে। |
| %o | এটি ব্যবহার করলে Octal Integer Data item  আউটপুট দিবে। |
| %p| এটি ব্যবহার করলে Pointer Data item আউটপুট দিবে। |
| %s | এটি ব্যবহার করলে String   Data item আউটপুট দিবে। |
| %u | এটি ব্যবহার করলে Unsigned decimal Data item আউটপুট দিবে। |
| %x | এটি ব্যবহার করলে Hexadecimal Data item আউটপুট দিবে।|


এবার আমরা scanf ও printf এর ব্যবহারের উপর একটি ছোট্ট প্রোগ্রাম দেখিঃ
```c
#include <stdio.h>
int main(void)
 
{
	char name[80];
	scanf("%s",&name);
	printf("You enter: %s",name);
	return 0;
}
```

এখানে একটি name নামে একটি character array (array সম্পর্কে পরে আলোচনা করা হবে) নেওয়া হয়েছে, যা মোট ৮০ টি character ধারন করতে পারবে(আসলে ৭৯ টি আরেকটি Null Character, যা সম্পর্কে পরে আলোচনা করা হবে) । তার পর এর মান ইনপুট ডিভাইস হতে নেওয়া হবে scanf function দ্বারা। scanf এর ভিতর %s দ্বারা বুঝানো হয়েছে যে এটি একটি String Input নিবে। তার পর এ মান printf(“%s”,name); দ্বারা পর্দায় আউটপুট দেখানো হয়েছে।