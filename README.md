# CSC-461-361-PA1-Programming-Assessment-solved

Download Here: [CSC 461/361 PA1 – Programming Assessment solved](https://jarviscodinghub.com/assignment/pa1-programming-assessment-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Submit program to perforce in your student directory o Sub directory called: /PA1/… o Fill out your PA1 Submission Report.pdf  Check it out and submit to same directory  There is nothing to Cut and Paste, leave it blank in the report  There are no tests to enter, leave it blank  Enter the final Changelist number of your PA1 submission
• Programming Assessment o Real world C++ exam that we give to interview candidates o Great practice
• Write all programs in cross-platform C or C++. o Optimize for execution speed and robustness. • Create a programming file for each problem, for example o Student directory – for this assignment only the CPP files submitted  /PA1/problem1.cpp  /PA1/problem2.cpp  /PA1/problem3.cpp  /PA1/problem4.cpp • Do all your work by yourself o Feel free to talk with others about setup, version control o DO NOT SHARE coding ideas on this assignment o Do not copy your friend’s code.  This is a competition! • Check in the problems multiple times, at least 4 times for this PA (programming assignment) o Have reasonable check-in comments • Make sure that your program compiles and runs o Warning level 4, some times that is not possible due to MS headers… o Your code should be squeaky clean. o There should be no warnings in the code that you did. • Read the instructions carefully o Optimize all code for Speed and Robustness o If you program doesn’t compile, it’s a zero. o If you submit a project make sure that minimum files are submitted  See perforce thread on how to submit minimum code o Most students do VERY poorly on this assignment  They are rushing and not thinking about this assignment correctly
Optimized C++ Programming Assignment 1
Optimized C++ PA -1 Fall 2015 Keenan o In the first class we go through all the optimizing ideas that you would need to successfully complete this assignment, please review • C++ fundamentals sometimes trip up students o Think about the interfaces  Clean simple robust interfaces are needed  Think about the end user, how would they call the functions o Should you use pointers, references, or value? o What external functions are you calling?  Look up each function, make sure you understand what each function does  Think about how it’s used from a performance point of view.  Can those routines give you errors? • We are using Perforce o You should have received the document describing how to login.  Please look at the documentation on the class website o IP and Port of the server:  IP: 140.192.39.61  PORT: 1666 o Submit program to perforce in your student directory  Sub directory called: /PA1/… • There is a sample problem4.cpp in that directory that you can use as a reference to refactor. (saves typing)
Simple check list to make sure that everything is checked in correctly • Did you do all 4 problems? • Do they compile and run without any errors? • Warning level 4 free? • Submitted it into /PA1 directory? • Can you delete you local drive, regrab the PA1 directory? o Is all the code there?
Most assignments will have hints in a section like this. • Do many little check-ins o Iteration is easy and it helps. o Perforce is good at it. • Think about performance, did you read the Code Complete chapters? o A lot of good ideas in there.

Optimized C++ Programming Assignment 2
Optimized C++ PA -1 Fall 2015 Keenan
Write all programs in cross-platform C or C++. o Optimize for execution speed and robustness.
1) (C/C++) Write a function to calculate this equation:

(Assume input: float x, output: float y.)
2) (C/C++) Write a function to normalize a 3 dimensional Cartesian vector.
3) (C/C++) Write a function that removes a given node in a linked list container containing nodes of type LinkList. Assume that each LinkList node and its data pointer were originally allocated dynamically by either malloc (C code) or new (C++ code). typedef struct LinkList { struct LinkList *next; struct LinkList *prev; struct ImportantData *data; } LinkList_t; LinkList_t *headList;
next
prev data
Node 0
next
prev data
Node 1
next
prev data
Node 2
next
prev data
Node N
0
0
Dynamically Allocated Memory
Dynamically Allocated Memory
Dynamically Allocated Memory
Dynamically Allocated Memory
headList
Optimized C++ Programming Assignment 3
Optimized C++ PA -1 Fall 2015 Keenan 4) (C/C++) The findMaxDistance() function (given below) calculates the maximum distance between any two players in the passed-in player array. Refactor it so that it also calculates the minimum distance between any two players. You may change the signature of the function and the contents of the function, but do not change the Vect_t structure. typedef struct Vect // Vector struct for positions { float x; float y; float z; } Vect_t; /*********************************************************************** * * Function: findMaxDistance() * * Input: * int nPlayers – number of players * Vect_t *playerArray – the array of players * Output: * float maxDist – the maxDistance between any two players * ***********************************************************************/ float findMaxDistance( int nPlayers, Vect_t *playerArray ) { int i,j; // counter variables Vect_t tmpVect; // temporary vector float tmpDist; // temporary distance float maxDist; // current max distance // initialize the distance to zero maxDist = 0.0f; for( i = 0; i < nPlayers; i++ ) { for( j = 0; j < nPlayers; j++ ) { // Find a vector between point i and j tmpVect.x = playerArray[i].x – playerArray [j].x; tmpVect.y = playerArray[i].y – playerArray [j].y; tmpVect.z = playerArray[i].z – playerArray [j].z; // Get its length tmpDist = (float)sqrt( tmpVect.x * tmpVect.x + tmpVect.y * tmpVect.y + tmpVect.z * tmpVect.z ); // determine if it’s a new maximum length if( tmpDist maxDist) { // yes so keep it maxDist = tmpDist; } } //for(j) } // for(i) return maxDist; } // End of findMaxDistance()
