# Mario

[![Watch the video](https://img.youtube.com/vi/cWOkHQXw0JQ/0.jpg)](https://youtu.be/cWOkHQXw0JQ?si=KBLDj4WxWwMAlMVE)

## Problem to Solve

Toward the end of World 1-1 in Nintendo’s [Super Mario Bros.](https://en.wikipedia.org/wiki/Super_Mario_Bros.), Mario must ascend right-aligned pyramid of bricks, as in the below.

![pyramid](https://github.com/user-attachments/assets/75f11048-15be-4de6-89ab-ad561af03adb)

In a file called `mario.c` in a folder called `mario-less`, implement a program in C that recreates that pyramid, using hashes (`#`) for bricks, as in the below:

```
       #
      ##
     ###
    ####
   #####
  ######
 #######
########
```
But prompt the user for an int for the pyramid’s actual height, so that the program can also output shorter pyramids like the below:
```
  #
 ##
###
```
Re-prompt the user, again and again as needed, if their input is not greater than 0 or not an `int` altogether.
<details>
<summary>Hints</summary>

- Recall that you can get an <code>int</code> from a user with <code>get_int</code>, which is declared in <code>cs50.h</code>.
- Recall that you can print a <code>string</code> with <code>printf</code>, which is declared in <code>stdio.h</code>.

</details>

## Demo

```
$ make mario
$ ./mario
Height: 8
       #
      ##
     ###
    ####
   #####
  ######
 #######
########
$ ./mario
Height: -3
Height: 3
  #
 ##
###
$
```

## Advice

Click the below toggles to read some advice!

<details>
<summary>Write some code that you know will compile</summary>
<br>
Even though this program won’t do anything, it should at least compile with <code>make</code>!
</br>
<pre>
#include <cs50.h>
#include <stdio.h>

int main(void)
{

}
</pre>
</details>

<details>
<summary>Write some pseudocode before writing more code</summary>

If unsure how to solve the problem itself, break it down into smaller problems that you can probably solve first. For instance, this problem is really two problems:

1. Prompt the user for the pyramid's height
2. Print a pyramid of that height

So write some pseudocode as comments that remind you to do just that:

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // Prompt the user for the pyramid's height

    // Print a pyramid of that height
}

<details>
<summary>Convert the pseudocode to code</summary>
<br>
First, consider how you might prompt the user for the pyramid’s height. Recall that a <code>do while</code> loop is helpful when you want to do something at least once, and possibly again and again, as in the below:
</br>
<pre>
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // Prompt the user for the pyramid's height
    int n;
    do
    {
        n = get_int("Height: ");
    }
    while (n < 1);

    // Print a pyramid of that height
}
</pre>

<br>
Second, consider how you might print a pyramid of that height, from top to bottom. Notice how the first row should have one brick, the second row should have two bricks, and so on. Odds are you’ll want a loop, as in the below, even if not (yet!) sure what to put in that loop. So add some more pseudocode as a comment for now:
</br>
<pre>
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // Prompt the user for the pyramid's height
    int n;
    do
    {
        n = get_int("Height: ");
    }
    while (n < 1);

    // Print a pyramid of that height
    for (int i = 0; i < n; i++)
    {
        // Print row of bricks
    }
}
</pre>

<br>
How to print that row of bricks? Well, wouldn’t it be nice if there were a function called print_row that could do just that? Let’s suppose that there is:
</br>
<pre>
#include <cs50.h>
#include <stdio.h>

void print_row(int bricks);

int main(void)
{
    // Prompt the user for the pyramid's height
    int n;
    do
    {
        n = get_int("Height: ");
    }
    while (n < 1);

    // Print a pyramid of that height
    for (int i = 0; i < n; i++)
    {
        // Print row of bricks
    }
}

void print_row(int bricks)
{
    // Print row of bricks
}
</pre>

<br>
We could then call that function from <code>main</code>, as in the below:
</br>
<pre>
#include <cs50.h>
#include <stdio.h>

void print_row(int bricks);

int main(void)
{
    // Prompt the user for the pyramid's height
    int n;
    do
    {
        n = get_int("Height: ");
    }
    while (n < 1);

    // Print a pyramid of that height
    for (int i = 0; i < n; i++)
    {
        // Print row of bricks
        print_row(i + 1);
    }
}

void print_row(int bricks)
{
    // Print row of bricks
}
</pre>

<br>
Why <code>i + 1</code>, though?
</br>
<br>
Let’s now implement <code>print_row</code>:
</br>
<pre>
#include <cs50.h>
#include <stdio.h>

void print_row(int bricks);

int main(void)
{
    // Prompt the user for the pyramid's height
    int n;
    do
    {
        n = get_int("Height: ");
    }
    while (n < 1);

    // Print a pyramid of that height
    for (int i = 0; i < n; i++)
    {
        // Print row of bricks
        print_row(i + 1);
    }
}

void print_row(int bricks)
{
    for (int i = 0; i < bricks; i++)
    {
        printf("#");
    }
    printf("\n");
}
</pre>

<br>
Why the <code>\n</code> at the end, though?
</br>
<br>
Unfortunately, this code prints a left-aligned pyramid, but you need a right-aligned one! Perhaps we should print some blank spaces before some of the bricks, to move them to the right? Let’s change <code>print_row</code> as follows so that it can print both:
</br>
<pre>
#include <cs50.h>
#include <stdio.h>

void print_row(int spaces, int bricks);

int main(void)
{
    // Prompt the user for the pyramid's height
    int n;
    do
    {
        n = get_int("Height: ");
    }
    while (n < 1);

    // Print a pyramid of that height
    for (int i = 0; i < n; i++)
    {
        // Print row of bricks
    }
}
void print_row(int spaces, int bricks)
{
    // Print spaces

    // Print bricks
}
</pre>
<br>
Some pseudocode now remains in both <code>main</code> and <code>print_row</code>, so that we leave to you!
</br>
<br>
And consider whether you could factor out some of the code in <code>main</code> to a <code>get_height</code> function, too, that returns the <code>int</code> you need!
</br>
</details>
