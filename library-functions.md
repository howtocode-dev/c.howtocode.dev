#লাইব্রেরী ফাংশন

ফাংশান হচ্ছে পুনরায় ব্যবহার যোগ্য কোড ব্লক। যা একটি নির্দিষ্ট কাজ করতে পারে। সি প্রোগ্রামিং এ এমন অনেক গুলো ফাংশন লেখা রয়েছে। যে গুলোকে বলা হয়  লাইব্রেরী ফাংশন। যেমন printf একটি ফাংশন, যার কাজ কোন কিছুর আউটপুট দেখা। আমাদের প্রতিটা প্রোগ্রামের শুরুতেই #include<stdio.h> লেখাটি যুক্ত করি। যার মানে আমরা এর আগেই জেনে এসেছি। মানে হচ্ছে Standard Library Functions টি যুক্ত করা। যেমন আমরা printf ব্যবহার করি, এটি হচ্ছে Standard I/O Functions এর একটা ফাংশন। Standard I/O এ আরো কিছু ফাংশন রয়েছে, যেমনঃ scanf(), getchar(), putchar() ইত্যাদি। এ গুলো সম্পর্কে পরবর্তী চ্যাপ্টার গুলো থেকে জানা যাবে।
নিচে কিচু include file এবং তাদের ফাংশন গুলো দেওয়া হলো। প্রতিটি include file এর ব্যবহার সম্পর্কে বিস্তারিত লেখা লিঙ্কে যুক্ত করা হয়েছে। লিঙ্ক থেকে বিস্তারিত উদাহরণ সহ দেখে নেওয়া যাবে।

কোন ফাংশনে যে মান পাস করা হয়, সে গুলোকে বলা হয়  আর্গুমেন্ট/Argument। কোন কোন লাইব্রেরী ফাংশন কোন Argument ছাড়াই কাজ করে। কোন কোন ফাংশন একটি Argument নেয়। আবার কোন কোন ফাংশন একের অধিক Argument নিয়ে কাজ করে।

##stdio.h: I/O functions:

* getchar() returns the next character typed on the keyboard.
* putchar() outputs a single character to the screen.
* printf() as previously described
* scanf() as previously described

 

 
 

#string.h: String functions

1. strcat() concatenates a copy of str2 to str1
2. strcmp() compares two strings
3. strcpy() copys contents of str2 to str1
 


 

##ctype.h: Character functions

* isdigit() returns non-0 if arg is digit 0 to 9
* isalpha() returns non-0 if arg is a letter of the alphabet
* isalnum() returns non-0 if arg is a letter or digit
* islower() returns non-0 if arg is lowercase letter
* isupper() returns non-0 if arg is uppercase letter

 

##math.h: Mathematics functions

* acos() returns arc cosine of arg
* asin() returns arc sine of arg
* atan() returns arc tangent of arg
* cos() returns cosine of arg
* exp() returns natural logarithim e
* fabs() returns absolute value of num
* sqrt() returns square root of num

 

##time.h: Time and Date functions

* time() returns current calender time of system
* difftime() returns difference in secs between two times
* clock() returns number of system clock cycles since program execution

 

##stdlib.h:Miscellaneous functions

1. malloc() provides dynamic memory allocation, covered in future sections
2. rand() as already described previously
3. srand() used to set the starting point for rand()
