# Note 03

## Compound data types

C uses `struct` to define a compound data type. Below are several examples.

* Spatial coordinates

  ```c
  struct coord {
      double x;
      double y;
      double z;
  };

* A body in space

  ```c
  struct body {
      struct coord coord;
      double mass;
  };

Compound data types are also called records or composite data types.

Let us define a variable `b` of type `struct body`:

```c
struct body b;
```

Then let us access its fields:

```c
b.mass;
b.coord;
b.coord.z;
```

## Pointers

Pointers hold the address of a memory location. In C, pointers have types.
For instance, we distinguish between a pointer to a character and a pointer to
an instance of `struct body`.

Here is the definition of a variable holding a pointer to a character:

```c
char *p1;
```

And there is the definition of a variable holding a pointer to a instance of
`struct body`:

```c
struct body *p2;
```

## Put it all together

Here is a fragment of code declaring an instance of `struct body` and initializing a variable with its address in memory:

```c
struct body b;
b.mass = 48984.08;
b.coord.x = 0.0;
b.coord.y = 0.0;
b.coord.z = 0.0;
struct body *p = &b;
```

The unary operator `&` returns the address of its operand.

## Dereferencing

Assume that `q` is a pointer to an integer. Then the expression `*q` returns
the integer pointed to by `q`. We say that the unary operator `*` dereferences
its operand. In layman's term, the unary operator `*` follows the pointer in
memory and returns the value stored there.

## Activities

Let us say that I want to create a list of real numbers. How would I define a
element of such a list in C?

Assume that `r` is a pointer to an instance of `struct body`. How do I access
its mass? How do I access its `y` coordinate?

Have you seen the `*` operator before? What about the `&` operator?
