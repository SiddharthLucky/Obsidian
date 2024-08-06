#BackendDeveloper #Java-Concepts 

- Thread Lifecycles:
    1. **New**: The thread is created but not yet started.
        - A thread is in this state when it is created using the `new` keyword, but the `start()` method has not been invoked.
    2. **Runnable**: The thread is ready to run and is waiting for CPU time.
        - A thread is in this state when it has been started and is eligible to run but may not actually be running due to CPU scheduling.
    3. **Blocked**: The thread is waiting for a monitor lock to enter or re-enter a synchronized block/method.
        - A thread is in this state when it is trying to acquire a lock that another thread holds.
    4. **Waiting**: The thread is waiting indefinitely for another thread to perform a particular action.
        - A thread is in this state when it calls `wait()`, `join()`, or `park()` methods without a timeout.
    5. **Timed Waiting**: The thread is waiting for another thread to perform a particular action within a specified waiting time.
        - A thread is in this state when it calls `sleep()`, `wait()`, `join()`, or `parkNanos()/parkUntil()` with a timeout.
    6. **Terminated**: The thread has completed its execution.
        - A thread is in this state when its `run()` method exits normally or due to an uncaught exception.
- **Advanced Concepts in Multithreading**:
    - Involves techniques such as thread synchronization, inter-thread communication, deadlock avoidance, and high-level concurrency utilities to manage multiple threads efficiently.
	1. **Thread Pools**:
	    - A thread pool is a managed collection of worker threads that efficiently execute asynchronous tasks by reusing a fixed number of threads instead of creating new ones for each task.
	2. **Executor Framework**:
	    - The Executor framework in Java provides a high-level API for managing and controlling thread execution, decoupling task submission from execution using interfaces like **`Executor`**, **`ExecutorService`**, and **`ScheduledExecutorService`**.
	3. **Synchronization Mechanisms**:
	    - Synchronization mechanisms like synchronized blocks/methods, **`Lock`** objects, **`volatile`** keyword, and **`Atomic`** classes ensure that shared resources are accessed by only one thread at a time, preventing race conditions.
	4. **Handling Concurrency Issues**:
	    - Involves techniques to address problems like deadlocks, race conditions, and thread starvation, using tools such as **`ReentrantLock`**, **`ReadWriteLock`**, **`Semaphore`**, and concurrent collections.
### **Interview Questions and Answers**

1. **What is a thread pool, and why is it used?**
    - **Answer**: A thread pool is a collection of reusable threads that execute tasks from a queue. It is used to improve performance by reducing the overhead of creating and destroying threads for each task, managing resources more efficiently.
2. **How does the Executor framework differ from traditional thread management?**
    - **Answer**: The Executor framework separates task submission from execution, allowing for better management of thread execution through a set of high-level APIs like **`ExecutorService`** and **`ScheduledExecutorService`**, simplifying concurrent programming.
3. **What are the different types of thread pools provided by the Executor framework?**
    - **Answer**: The Executor framework provides several types of thread pools, including **`FixedThreadPool`**, **`CachedThreadPool`**, **`SingleThreadExecutor`**, and **`ScheduledThreadPoolExecutor`**, each suited for different use cases.
4. **How do you achieve thread safety in Java?**
    - **Answer**: Thread safety can be achieved using synchronization mechanisms such as synchronized blocks/methods, **`ReentrantLock`**, **`ReadWriteLock`**, **`volatile`** keyword, and concurrent collections like **`ConcurrentHashMap`**.
5. **What is a `volatile` keyword in Java, and when would you use it?**
    - **Answer**: The **`volatile`** keyword ensures that changes to a variable are immediately visible to all threads, preventing threads from caching the variable's value. It is used for flags or state variables that are shared between threads but not involved in compound actions.
6. **What is a deadlock, and how can it be avoided?**
    - **Answer**: A deadlock occurs when two or more threads are blocked forever, waiting for each other to release resources. It can be avoided by using a consistent locking order, avoiding nested locks, and using timeout locks.
7. **Explain the concept of a `ReentrantLock` and how it differs from a synchronized block.**
    - **Answer**: **`ReentrantLock`** is a flexible and extensible lock implementation that provides more control over locking, such as timed, interruptible, and fair locking. Unlike synchronized blocks, **`ReentrantLock`** allows for explicit lock unlocking and reentrance, which means the same thread can acquire the lock multiple times without deadlock.
8. **What are `Atomic` classes, and why are they used?**
    - **Answer**: **`Atomic`** classes (like **`AtomicInteger`**, **`AtomicReference`**) provide thread-safe operations for single variables without using locks, relying on low-level atomic machine instructions to ensure visibility and atomicity.
9. **What is a `Semaphore`, and how is it used in Java?**
    - **Answer**: A **`Semaphore`** is a synchronization aid that controls access to a resource by multiple threads through permits. It can be used to enforce limits on resource usage, allowing a set number of threads to access a resource simultaneously.
10. **What is the difference between `wait()` and `sleep()` in Java?**
    - **Answer**: **`wait()`** is used for inter-thread communication, causing the current thread to release the monitor and wait until another thread invokes **`notify()`** or **`notifyAll()`** on the same object. **`sleep()`** simply pauses the current thread for a specified time without releasing any locks or monitors.