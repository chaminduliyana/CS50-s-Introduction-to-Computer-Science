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

Even though this program won’t do anything, it should at least compile with `make`!

``` c
#include <cs50.h>
#include <stdio.h>

int main(void)
{

}
```

</details>

<details>
<summary>Write some pseudocode before writing more code</summary>

If unsure how to solve the problem itself, break it down into smaller problems that you can probably solve first. For instance, this problem is really two problems:

1. Prompt the user for the pyramid’s height
2. Print a pyramid of that height
So write some pseudcode as comments that remind you to do just that:

``` c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // Prompt the user for the pyramid's height

    // Print a pyramid of that height
}
```

</details>
