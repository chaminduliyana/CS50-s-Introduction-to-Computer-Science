# Hello, It’s Me

[![Watch the video](https://img.youtube.com/vi/YQHsXMglC9A/0.jpg)](https://youtu.be/YQHsXMglC9A?si=S_d9V5XUZurN-l4c)

## Problem to Solve

In a file called `hello.c`, in a folder called `me`, implement a program in C that prompts the user for their name and then says hello to that user. For instance, if the user’s name is Adele, your program should print `hello, Adele\n`!

<details>
<summary>Hints</summary>

- Recall that you can get a <code>string</code> from a user with <code>get_string</code>, which is declared in <code>cs50.h</code>.
- Recall that you can print a <code>string</code> with <code>printf</code>, which is declared in <code>stdio.h</code>.
- Recall that you can format a <code>string</code> with <code>printf</code> with <code>%s</code>.

</details>

## Demo

```
$ make hello
$ ./hello
What's your name? Adele
hello, Adele
$ ./hello
What's your name? David
hello, David
$
```
## How to Begin

Execute `cd` by itself in your terminal window. You should find that your terminal window’s prompt resembles the below:
```
$
```
Next execute
```
mkdir me
```
to make a folder called `me` in your codespace.

Then execute
```
cd me
```
to change directories into that folder. You should now see your terminal prompt as `me/ $`. You can now execute
```
code hello.c
```
to create a file called `hello.c` in which you can write your code.

## Walkthrough

Here’s a “walkthrough” (i.e., tour) of this problem, if you’d like a verbal overview of what to do too!

[![Watch the video](https://img.youtube.com/vi/wSk1KSDUEYA/0.jpg)](https://youtu.be/wSk1KSDUEYA?si=unmhkfrRue4Gti-i)

## How to Test

### Correctness
In your terminal, execute the below to check your work’s correctness.
```
check50 cs50/problems/2024/x/me
```

### Style
```
style50 hello.c
```
### How to Submit
```
submit50 cs50/problems/2024/x/me
```


