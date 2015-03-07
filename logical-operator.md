#লজিক্যাল অপারেটর
Relational and Logical Operators গুলো হল:

1. Relational  Operators
2. Equality Operator
3. Logical Operator

 

C programming language এ চার প্রকার  Relational Operator রয়েছে:


|Operator | Meaning |
| -- | -- |
| < | Less then |
|<= | Less then or equal to |
| >	 | Greater then |
| >= | Greater then or equal to |
 


	
	
	

	
মনে করি x, y দুটি চলক। x এর মান 5,  y এর  মান 6। সুতরাং x<y  এর মানে হচ্ছে x y থেকে ছোট অর্থাৎ x<y  expression টি সত্য এবং এর মান হবে 1. আবার x>y  expression টি মিথ্যে এবং এর মান হবে 0.
Relational Operator ব্যবহার করে আমরা সহজেই দুটি সংখ্যার মধ্যে কোনটা ছোট তা বের করে ফেলতে পারি। যা আমরা এর পরের অধ্যায় if – else অংশে  দেখব।

##Equality Operator:

RELATIONAL OPERATOR এর সাথে সম্পর্ক যুক্ত দুটি Equality Operator রয়েছে। নিচে এদের দেওয়া হলঃ

| Operator | Meaning |
| -- | -- |
| == | Equal to |
| != | Not Equal to |

	
	
	
এখানে প্রথম টি হচ্ছে দুটি সমান চিহ্ন। দুটি মিলেই Equal to  Operator প্রকাশ করে। দ্বিতীয় টি হচ্ছে একটি !(উচ্চারন নট) ও একটি সমান চিহ্ন নিয়ে Not Equal to  Operator প্রকাশ করে।

উদাহরনঃ মনে করি x, y দুটি চলক। x এর মান 5. Y এর মান 6। সুতরাং x==y এর মানে হচ্ছে x এবং y এর মান সমান। কিন্ত আমদের x এবং y এর মান সমান নয়। সুতরাং x==y  expression টি মিথ্যে এবং এর মান হবে 0. আবার x!=y (উচ্চারন x not equal to y) হয় তাহলে expression টি সত্য হয় এবং এর মান হবে 1.

এখানে মনে রাখতে হবে যে Assignment operator = এবং Equality Operator == সম্পূর্নই ভিন্ন। কোন মান বা Value কোন Identifier এর মধ্যে assign বা নির্দিষ্ট করার জন্য assignment operator ব্যবহৃত হয়। আর যেখানে দুইটা Expression এর মান সমান হলে Equality Operator == ব্যবহার করা হয়। Equality Operator দ্বারা Logical True অথাবা False নির্নয় করা হয়।

এখানে একটার স্থানে আরেকটা কোন অবস্থাতেই বসানো যাবেনা। তাহলে Program এ বিশাল ভুল আসবে। প্রথম প্রথম অনেকেই এই ভুল করে।

##LOGICAL OPERATOR:

C প্রোগ্রামিং এ দুটি Logical Operator রয়েছে। তাদের নিচে দেওয়া হলঃ

| Operator |Meaning |
| -- | -- |
| && | And |
|   | Or |

	
	
	
&& কে বলা হয় Logical and এবং || কে বলা হয় Logical Or.

##&&(পড়া হয় And)  operator :

মনে করি x,y,z তিনটি চলক। এখন (x<y)&& (y<z) হচ্ছে একটি expression. এখন এর মান সত্য হবে যদি (x<y) এবং (y<z) সত্য হয়। (x<y) এবং (y<z) এর যে কোন একটি মিথ্যা হলে (x<y)&& (y<z) এর মান মিথ্যে হবে।

##||(পড়া হয় Or Or)  operator :

মনে করি x,y,z তিনটি চলক। এখন (x<y)||(y<z) হচ্ছে একটি expression. এখন এর মান সত্য হবে যদি (x<y) এবং (y<z) সত্য হয়। অথবা (x<y) এবং (y<z) এর যে কোন একটি সত্য হয়। (x<y) এবং (y<z) দুটি একসাথে মিথ্যা হলে (x<y)||(y<z) এর মান মিথ্যে হবে।

###RELATIONAL AND LOGICAL OPERATORS এর কয়েকটি উদাহরন নিচে দেওয়া হল:

মনে করি x, y, z তিনটি চলক। x এর মান 5. y এর  মান 6 এবং z এর মান 7।

Expression	ব্যাখ্যা	মান
 