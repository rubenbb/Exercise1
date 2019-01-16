
All three programs uses two threads and execute the functions partly each. As the memory is shared, they both will have access to the memory at the same time, leading to conflicts. The value of i can be reached by one thread before the other thread saves its updated value, leading to different results, depending on the runtime of each thread.
