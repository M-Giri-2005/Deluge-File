//1) Write a Deluge Script to find and display the longest word in a given string along

// with the number of letters it contains.

//  input ->  words="Hi my name is Batman Harik";

// output -> Batman : 6 letters.



inputvalue="Hi my name is Batman Harikumar";

var=inputvalue.toList(" ");

new="";

for each i in var

{

 	if(new.length()<i.length())

 	{

 		new=i;

 	}

}

info new;

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

// 2)Write a Deluge script to check whether two lists have the same elements in same

// index. If both sets contain exactly the same elements, print "same"; otherwise,

// print "Not same".

//  input ->  a={4,5,6} b={4,5,6}

// output -> same

//  input ->  a={4,5,6} b={4,5,-1,22}

// output -> Not same



a={4,6,5};

b={4,5,6};

if(a.equalsIgnoreCase(b))

{

 	info "same";

}

else

{

info "not same";

}



//another method



a={5,4,6,8,10};

var=a.size();

b={4,5,8,6,10};

var1=b.size();

count=0;

for each i in a

{

 	for each g in b

    {

 		if(i==g)

 		{

 			count+=1;

 		}



    }

}

if(var==count \&\& var1 == count)

{

 	info "same";



}

else

{

 	info "Not Same";

}



//another Method



a={5,4,6,8};

b={4,5,8,6,10};

for each i in a

{

 	for each k in b

    {

 		if(i==k)

 		{

 

 			a.removeElement(i);

 			b.removeElement(k);

 		}

    }

}

if(a.isBlank() \&\& b.isBlank())

{

 	info "same";

}

else

{

 	info "Not Same";

}

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

//  3. Write a Deluge Script to check whether a given list is a palindrome.

//  A list is considered a palindrome if it reads the same forwards and backwards.

//  input ->  a={3,4,5,4,3};

// output -> Palindrome

//  input ->  a={3,3,4,5};

// output -> Not Palindrome



inputvalue={3,4,5,4,3};

newlist=list();

count=inputvalue.size()-1;

for each i in inputvalue

{

 	newlist.add(inputvalue.get(count));

 	count-=1;

}

if(inputvalue==newlist)

{

 	info "Palindrom";

}

else

{

 	info "Not Palindrom";

}

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

**Intermediate**



// 1. Write a Deluge Script to find the maximum difference between any two

// consecutive elements in a list after sorting it in ascending order.

//  Print that maximum difference.

//  Input -> numList = {2,4,6,1}

//  Output ->  2

//  Explanation -> The sorted form of the array is \[2,4,6,1], either (2,4) or (4,6) has the

// maximum difference 2



firstlist={2,4,6,1};

space="".rightPad(firstlist.size()).toList("");

space.removeElement(space.get(space.size()-1));

nextlist=list();

loopcount=0;

for each i in space

{

 	nextlist.add(firstlist.get(loopcount+1)-firstlist.get(loopcount));

 	loopcount+=1;

 

}

finalvalue=map();

for each i in nextlist

{

 	if(finalvalue.containKey(i))

 	{

 		var=finalvalue.get(i)+1;

 		finalvalue.put(i,var);

 	}

 	else

    {

 		finalvalue.put(i, 1);

    }

}

a=finalvalue.values().sort(false);

info finalvalue.getkey(a.get(0));



**\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\***











































































**\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*ANOT
HER PDF\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\***



1)Write a Deluge Script to design the below attached patterns



var="".leftPad(5).toList("");

count=1;

for each i in var

{ 

&nbsp;	info "  \*   ".repeat(count);

&nbsp;	count+=1;

}

info "-------------------------------------------------";

// \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

var="".leftPad(5).toList("");

count=5;

for each i in var

{

&nbsp;	info "  \*  ".repeat(count);

&nbsp;	count-=1;

}



info "---------------------------------------------------";



// \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*



var="".leftPad(5).toList("");

spacecount=5;

loopcount=1;

for each j in var

{

&nbsp;	info " ".leftpad(spacecount \*3)+" \*".repeat(loopcount);

&nbsp;	loopcount+=2;

&nbsp;	spacecount-=1;

&nbsp;	

}

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*



**// 2. Write a Deluge script to sort a list of numbers such that:**

**// 2.1 All negative numbers appear first in descending order**

**//  2.2 All positive numbers appear next in ascending order,**

**// 2.3 Any null (or None) values should appear at the beginning of the list.**

**//  Input -> numbers = \[10, 2, -4, 90, 999, -1000, 1, 35, None]**

**// Output -> \[None, -4, -1000, 1, 2, 10, 35, 90, 999]**



**firstlist={10,2,-4,90,999,-1000,1,35,"None"};**

**negative=list();**

**positive=list();**

**emty=list();**

**finallist= list();**

**for each i in firstlist**

**{**

\*\*if (i== "None"|| i == "Null")\*\*

	\*\*{\*\*

			\*\*emty.add(i);\*\*

	\*\*}\*\*

	\*\*else if(i>=0)\*\* 

    \*\*{\*\*

		\*\*positive.add(i);\*\*

    \*\*}\*\*

	\*\*else if(i < 0)\*\*

    \*\*{\*\*

	

		\*\*negative.add(i);\*\*

    \*\*}\*\*


**}**

**negative.sort(false);**

**positive.sort();**

**finallist.addAll(emty);**

**finallist.addAll(negative);**

**finallist.addAll(positive);**

**info finallist;**

