## Part 3

### Question 1 (Joe)

>Why do we need locks for `browser_list` and `session_list` in `browser_handler()`? What could happen if there is no lock?

If the index into either list shifts or the state of a session/browser changes during the execution of this function, it could result in unexpected or undefined behavior.

### Question 2 (Joe)

> Can we use multiprocessing instead of multithreading here? What are the differences between multiprocessing and multithreading?

We can; we could, for instance, spawn an entirely separate server for each client. However, this would be fairly inefficient since we would be creating an entirely new copy of the program versus just "extending" one program.

