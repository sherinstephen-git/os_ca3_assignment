# os_ca3_assignment
OS_Assignment_CA3\
Roll no -43\
Name : Sherin Stephen\
id - 11807129\
section : k18GT\
Q1)The Fibonacci sequence is the series of numbers 0, 1, 1, 2, 3, 5, 8, .... Formally, it can be\
expressed as:\
f ib0 = 0\
f ib1 = 1\
f ibn = f ibn−1 + f ibn−2\
Write a multithreaded program that generates the Fibonacci sequence. This program should work\
as follows: On the command line, the user will enter the number of Fibonacci numbers that the\
program is to generate. The program will then create a separate thread that will generate the\
Fibonacci numbers, placing the sequence in data that can be shared by the threads (an array is\
probably the most convenient data structure). When the thread finishes execution, the parent\
thread will output the sequence generated by the child thread. Because the\
parent thread cannot begin outputting the Fibonacci sequence until the child thread finishes, the\
parent thread will have to wait for the child thread to finish.\
solution -\
Algorithm -\
Fibin(n)\
1 if(n<=1)\
2        return n\
3else x = Fibin(n-1)\
4        y=Fibin(n-2)
5        return x+y\
complexity -\
T(n) = T(n − 1) + T(n − 2) + Θ(1)\
T(n) = Θ(Fn)\


Q2)Consider a scenario of demand paged memory. Page table is held in registers. It takes 8\
milliseconds to service a page fault if an empty page is available or the replaced page is\
not modified and 20 milliseconds if the replaced page is modified. Memory access time is\
100 nanoseconds. Assume that the page to be replaced is modified 70 percent of the time.\
Generate a solution to find maximum acceptable page-fault rate for access time that is not\
more than 200 nanoseconds.\
solution algoritm - Time taken for empty page or unmodified page = 8ms.\
Time taken for modified page = 20ms\
memory access time = 100ns\
effective Access time = 200ns\
      EAT = (1-p)*(100) + (p)*(100 + (1-.7)*(8msec) + (.7)*(20msec)) \  
	  = 100 - 100p + 100p + (2.4e6)*p + (14e6)*p\
	  = 100 + (16.4e6)*p\
      200 = 100 + (16.4e6)*p\
      p = 100/16.4e6 = 6.0975609756097560975609756097561e-6 ~ 6.01e-6\
      p = page Fault Rate\


