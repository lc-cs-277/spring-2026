# Lab #1: Squaring and Copying

This assignment is meant to give you a chance to renew acquaintances with C. It
will also serve to highlight some, hopefully unexpected, behaviors of C.

## Which text editor?

I strongly suggest that you use one of three possible text editors listed below.
Word or Google Docs will not do. It doesn't matter much which editor you choose,
but its use should be become second nature over the course of the semester (and
beyond).

vim
* modal text editor
* start the tutorial: run the app `vimtutor` at the terminal
* rescue key: `esc`
* bailout: `esc` then `:wq`

emacs
* non-modal text editor
* start the tutorial: run the app `emacs` at the terminal then type `ctrl-h t`
* rescue key: `ctrl-g`
* bailout: `ctrl-x ctrl-c`

Visual Studio Code
* non-modal text editor
* here is a
  [link](https://code.visualstudio.com/docs/getstarted/getting-started) to getting started

## Squaring the ints

Write a program, called `squares.c` that outputs the squares of 5, 50, 500,
5,000, ..., 5,000,000, one square per line.

The output should look like so, exactly:

```
      5 25
     50 2500
    500 250000
...
```

Anything strange happening in the output? Discuss with a classmate.

## Copying

Write a program, called `copy.c` that contains two functions with similar
prototypes:

```c
void copy(int src[2048][2048], int dst[2048][2048]);
void copy2(int src[2048][2048], int dst[2048][2048]);
```

Both functions should copy the entire two-dimensional array `src` to the
two-dimensional array `dst`. For both functions, you should write two nested
loops, one iterating over the first index of the array with, say, variable `i`
and the other iterating over the second index with variable `j`. The only
difference between the two functions should be which index is being modified by
the outer loop. In `copy`, the outer loop should use `i`; in `copy2`, the outer
loop should use `j`. In other words, swap the two loops in `copy2`. Access to
array elements should remain `src[i][j]` and `dst[i][j]` in both functions.

Let time it takes for these two functions to complete their job. For this
purpose let us use the following function definition.

```c
#include <time.h>
const unsigned long billion = 1000000000ULL;
/**
 * Return the current time in nanoseconds.
 */
unsigned long time_get() {
	struct timespec t;
	clock_gettime(CLOCK_REALTIME, &t);
	return billion * t.tv_sec + t.tv_nsec;
}
```

Here is a starting point for the definition `main` function and some
declarations:

```c
int main() {
    unsigned long before, delta;

    before = time_get();
    copy(a, b);
    delta = time_get() - before;
    ...
}
```

The output of your program should be formatted as follows exactly (except for
the width of the numbers):

```
copy time:  ... ns
copy2 time: ... ns
```

Notice anything strange? Are the measurements repeatable?

## What to hand in

Upload `squares.c` and `copy.c` directly to [Google
Classroom](https://classroom.google.com/c/ODI4NDU3NDAyNTU0). These files should
already be "text" files; no need for conversions.
