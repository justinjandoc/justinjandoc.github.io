---
draft: false
layout: essay
type: essay
title: Pockets Full of (ES)Lint
date: 2022-02-08
labels:
  - Coding Standards
  - Learning
  - Software Engineering
---

## Side of Spaghetti

<img class="ui large right floated image" src="../images/spaghetti-code.png">

When doing anything, it is oftentimes natural to come across a certain style and sitck with it, making it your new standard. With practice, this becomes second nature and less of something that you go out of your way to do. As a second year Computer Science student in his fourth programming focused course, I believe I have a grasp on how I should incorporate my own style with my courses' established coding standards. Besides, the most restrictive coding standards can't be as bad as spaghetti code, right?

## Complying for Compiling

During my first course in the Computer Science program, there was no established coding standard. We were left to figure out how we wanted to format code and it was a bit exciting. My next two courses provided us with actual coding standards we would need to abide to, with the latest one overshadowing whatever style I created for myself.

```
// BAD
int getIndex(arr, num) {
    int i;
    for (i = 0; i < arr.length; i++) {
        if (arr[i] == num) {
            return i;
        }
    }
    return -1;
}

// GOOD
int getIndex(arr, num) 
{
    int i, ret = -1;
    for (i = 0; i < arr.length; i++) 
    {
        if (arr[i] == num) 
        {
            ret = i;
            i = arr.length;
        }
    }
    return ret;
}
```

I have to admit, moving on from that class and being able to do such forbidden acts such as having multiple return statements and not making a new line for curly braces fits better to my own personal preferences. However, I do believe that not having these standards would have been very detrimental to me. I spent more hours staring at my code trying to debug than actually writing it out. Because of this, having curly braces in their own lines so they are easier to see or having a variable whose sole purpose is to be returned rather than having to chase around numerous return statements has greatly reduced what should have been my debugging time.

It only makes sense though, such coding standards are established by professionals who have been in this field for years. 

## Red Lines

<img class="ui large banner centered floated image" src="../images/eslint-logo.png">


Currently, I am learning JavaScript and this course requires our code to be checked by ESLint. The coding standards required nicely fit with my own personal preferences. One the major advantages of using ESLint is that the excessive need to destroy those red lines may lead you to learning more about the JavaScript coding language.

The most common error I come across is how I declare my variables. I tend to go for what I thought was the safer pick, declaring my veriables with `let`. I surmised that using `const` was riskier, as you would not want to incremenent a constant variable. However, with the input of ESLint, I now understand the nature of `let` and `const` variables a little bit more. 

There are numerous other errors I have made, but ESLint has made it easier to fix these. All it takes is a few mouse clicks and my code is automatically fixed to adhere to the standards. Without this feature, ESLint would have been extremely tedious to use, as that would require things such as reading documentation to even have a grasp on why a block of code is _improper_.

ESLint will only help me shape my own personal preferences, as well as give me good coding standards that will allow me and others to easily read the programs I write. Having a consistent style is something nice that you should always have in your pocket.
