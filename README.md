java c
Electrical Engineering  Computer Science
EECS 281: Data Structures and Algorithms
Fall 2024
PRACTICE MIDTERM EXAM
KEY 1
Multiple Choice Portion [60 points]
MULTIPLE CHOICE INSTRUCTIONS:
•  Select only ONE answer per multiple choice question.
•  There are 24 multiple choice questions worth 2.5 points each.
•  Record your choices for all multiple choice questions using the circles in the boxed area next to each question. Use a number 2 pencil, not a pen (so that you may change your answer).  Fill the circle completely. There is no partial credit for multiple-choice questions.  Make sure you bubble in the correct letter. See the example below for how to select your answer.
•  There is no penalty for wrong answers: it is to your benefit to record an answer to each multiple- choice question, even if you’re not sure what the correct answer is.
•  The questions vary in difficulty — try not to spend too much time on any one question. Use your time wisely.
•  When asked about memory complexity, consider all possible sources (stack and heap).
•  The term "heap" as a data structure refers to a binary heap, unless explicitly stated otherwise.
•  The term "binary search tree" refers to a standard implementation that does not self-balance, unless explicitly stated otherwise.

1.   Master Theorem






Which of the following recurrence relations can one solve by applying the Master Theorem?
A)  T(n) = 2/1T(4/n) + Θ(n)
B)  T(n) = T(2/n) + Θ(nlog2 4)
C)  T(n) = 4T(n — 1) + Θ(1)
D)  T(n) = 4T(2/n) + 2T(4/n) + Θ(n2)
E)  None of the above.
2.   Measuring Runtime





Consider the following function:
1       int  func(double  m,  double  n)  {
2                int  c  =  0;
3              while   (m  >  n)  {
4                          m  =  m/2;
5                           for   (int  i  =  1;  i  <  n;  i *=3;) 
6                                      ++c;
7                }  //  while
8
9                return  c;
10        }  //  func
What best characterizes the running time of a call to this function?
A)  O(nlog m)
B)  O( log n)
C)  O((log ) · (log n))
D)  O(mnlog(mn))
E)  O(mn · (log m) · (log n))


3.   Math Foundations





Which of the following is NOT true regarding logarithms?
A)  log2 (n) = O(log3 (n))
B)  log3 (n) = O(log2 (n))
C)  log2 (n!) = O(nlog2 (n))
D)  log2 (n) = Θ(log3 (n))
E)  All of the above are true
4.   Complexity Analysis





Iff(n) = O(g(n)), and f(n) = Ω(h(n)) and f(n), g(n), and h(n) are strictly increasing functions, which of the following MUST be true?
A)  g(n) = O(h(n))
B)  g(n) = Θ(h(n))
C)  g(n) = Ω(h(n))
D)  g(n) = Θ(f(n))
E)  None of the above

5.   Recursion






Consider the following recurrence relation:


T(n) = {c0, n             n= 1
nT(n - 1) + c, n>1


What is the complexity of T(n)?
A)  Θ(nlog n)
B)  Θ(n2 )
C)  Θ(n3 )
D)  Θ(cn )
E)  Θ(n!)
6.   Queues



What is the best possible space complexity for a function printing out the contents of a std::queue of size n in order, such that the contents and order of the queue are the same before and after the function is called and executed?  This means the auxiliary, or additional, space required to make this occur, not the space taken up by the data that was in the queue to begin with. You can assume that the queue is passed by reference.
A)  O(1)
B)  O(n)
C)  O(n2 )
D)  O(n3 )


7.   Code Analysis





NOTE: Same code as next page, different question
Consider an array data of size n which contains 0s and 1s.  Each element of this array containing 0 appears before all those elements containing 1. For example, [0, 0, 0, 0, 1] is such an array.
1       int  myFunction(int  data[],  int  length)  {
2                  int  mid  =  0,  left  =  0;  int  right  =  length  -  1;
3                  if   (data[0]  ==  1)
4                             return  0;
5                  else  if   (data[length  -  1]  ==  0)
6                             return  length;
7                  else  {
8                             bool  isFound  =  false ;
9                             while   (!isFound)  {
10                                        mid  =  left  +   (right  -  left)  /  2;
11                                        if   (data[mid]  ==代 写EECS 281: Data Structures and Algorithms Fall 2024 PRACTICE MIDTERM EXAM KEY 1Web
代做程序编程语言  0)
12                                                    left  =  mid  +  1;
13                                        else  {
14                                                   if   (data[mid  -  1]  ==  0)
15                                                               isFound  =  true ;
16                                                   else
17                                                               right  =  mid  -  1; 18                                         }  //  else
19                              }  //  while
20                             return  mid;
21                   }  //  else
22        }  //  myFunction()
In general, what does the function return when it is given such an array?
A)  Number of 0’s in data[]
B)  Number of 1’s in data[]
C)  (Number of 0’s in data[]) + 1
D)  (Number of 1’s in data[]) + 1
E)  (Number of 1’s in data[]) - 1
8.   Complexity of Code





NOTE: Same code as previous page, different question
Consider an array data of size n which contains 0s and 1s.  Each element of this array containing 0 appears before all those elements containing 1. For example, [0, 0, 0, 0, 1] is such an array.
1       int  myFunction(int  data[],  int  length)  {
2                  int  mid  =  0,  left  =  0;  int  right  =  length  -  1;
3                  if   (data[0]  ==  1)
4                             return  0;
5                  else  if   (data[length  -  1]  ==  0)
6                             return  length;
7                  else  {
8                             bool  isFound  =  false ;
9                             while   (!isFound)  {
10                                        mid  =  left  +   (right  -  left)  /  2;
11                                        if   (data[mid]  ==  0)
12                                                    left  =  mid  +  1;
13                                        else  {
14                                                   if   (data[mid  -  1]  ==  0)
15                                                               isFound  =  true ;
16                                                   else
17                                                               right  =  mid  -  1; 18                                         }  //  else
19                              }  //  while
20                             return  mid;
21                   }  //  else
22        }  //  myFunction()
What is the complexity of the above algorithm?
A)  Θ(1)
B)  Θ(log(log n))
C)  Θ(log n)
D)  Θ(n)
E)  Θ(nlog n)
9.   Heaps and Heapsort





Which of the following is TRUE about binary heaps and heapsort?
A)  Finding the maximum element in a min heap tree has a complexity of Θ(log n)
B)  Turning a random set of elements into a heap has a complexity of Θ(log n)
C)  If the priority of one element in a heap changes, fixing the heap requires a minimum of Θ(n) operations
D)  The worst-case time complexity of heapsort is Θ(n2 )
E)  Heapsort can be implemented with O(1) additional space
10.   Binary Heaps




Which of the following represents a valid binary heap?

11.   Heaps




Suppose that we wanted to add a function popRandom() to our priority queues in Project 2.  When implementing it with the binary heap, we could generate a random index, swap values between that index and the last element of the data vector, and call the vector’s pop_back() function.  What else would we have to do to preserve the binary heap property?  Choose the answer with the smallest worst-case complexity.
A)  Call update_priorities().
B)  Call fixDown() followed by fixUp(), both on the random index.
C)  Call fixDown(), starting at the root of the heap.
D)  Call fixUp(), starting at the last element of the heap.
E)  Call exactly one of fixUp() or fixDown(), depending on the values swapped.
12.   Reversing an Array




You are asked to reverse the order of an arbitrary array of length n in constant memory.  Your code skeleton looks like:
1       for   ( . . . )  {
2                    std::swap(array[i],  array[n  -  i  -  1]); 
3        }
What belongs in the for loop header?
A)  for   (size_t  i  =  0;  i  <  n;  ++i)
B)  for   (size_t  i  =  0;  i  <   (n  /  2);  ++i)
C)  for   (size_t  i  =  n;  i  >=  0;  --i)
D)  None of the above
         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
