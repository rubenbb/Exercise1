# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency: Parallell activities that do not interact with eachother, while parallelism is when parallel activity shares the same resource. One task is divided into several subtasks, where each is solved on different cores at the same time.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *As we reach a limit for the clock speed of one processor, we can increase the overall number of tasks by introduce multiple cores, where each does one specific task*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *We can solve multiple, indepentant tasks simultaniously*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *As it makes the program more complicated, it would become harder.*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > *A process is the instance of a computer program that is being executed. This process consists of multiple threads, where each is the smalles sequence of programmed instructions. Green threads are threads that are scheduled by the user on an ordinary user-level process, not by the operating system. Coroutine is a thread that doesn't map on a native thread, meaning it doesn't require context switching on multiple processors. This leads to it being faster.*
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *- The command pthread_create() will create a thread in C
 - The python command threading.thread will create a thread
 - The go command in go will create a lightweigh thread, meaning it is a corountine.
 *
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *It protecs the object by syncronizing the threads such that only one can be executed at a given time.*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *An alternative interpreter can be used.*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *Sets the maximum number of processors that can execute simultaniously*
