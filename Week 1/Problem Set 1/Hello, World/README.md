# Hello, World

[![Watch the video](https://img.youtube.com/vi/ufB53UE2Cvo/0.jpg)](https://www.youtube.com/watch?v=ufB53UE2Cvo&t=103s)

# Problem to Solve
Thanks to Professor [Brian Kernighan](https://en.wikipedia.org/wiki/Brian_Kernighan) (who taught CS50 when David took it!), “hello, world” has been implemented in hundreds of languages. Let’s add your implementation to the list!
In a file called `hello.c`, in a folder called `world`, implement a program in C that prints `hello, world\n`, and that’s it!

# How to Begin

Open [VS Code](https://cs50.dev/).

Start by clicking inside your terminal window, then execute cd by itself. You should find that its “prompt” resembles the below.
```
$
```
Next execute
```
mkdir world
```
to make a folder called `world` in your codespace.

Then execute
```
cd world
```
to change directories into that folder. You should now see your terminal prompt as `world/ $`. You can now execute
```
code hello.c
```
to create a file called `hello.c` in which you can write your code.

# How to Test

Recall that you can compile `hello.c` with:
```
make hello
```
If you don’t see an error message, it compiled successfully! You can confirm as much with
```
ls
```
which should list not only `hello.c` (which is source code) but also `hello` (which is machine code).

If you do see an error message, try to fix your code and try to compile it again. If you don’t understand the error message, though, try executing
```
help50 make hello
```
for advice.

Once your code compiles successfully, you can execute your program with:
```
./hello
```

# Correctness
Execute the below to evaluate the correctness of your code using check50, a command-line program that will output happy faces whenever your code passes CS50’s automated tests and sad faces whenever it doesn’t!
