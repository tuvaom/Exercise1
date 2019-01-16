# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is when two or more tasks can start, run, and complete in overlapping time periodes. It does not mean that they will ever both be running at the same instant( nessesarily). Parallelism is when tasks actually run at the same time. 
 
 ### Why have machines become increasingly multicore in the past decade?
 > Because of high demands for speed and data.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Latency problems
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Your answer here*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Processes: is threads working within its own shared memory context.
 Threads: is the unit of parallelism and belongs to a certain process. 
 green threads: are threads that are sceduled by a runtime libary
 coroutines: Coroutines are computer-program components that generalize subroutines for non-preemptive multitasking, by allowing multiple entry points for suspending and resuming execution at certain locations
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > creates a new thread 
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > the global interpreter lock, or GIL, is a mutex that protects access to Python objects, preventing multiple threads from executing Python bytecodes at once
  Effectively makes any CPU-bound Python program single-threaded.

 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > 	You can run multiple python interpreters separately to get concurrent processes. Resource sharing can then be implemented with sockets
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > The GOMAXPROCS variable limits the number of operating system threads that can execute user-level Go code simultaneously.