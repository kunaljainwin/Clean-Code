# Clean-Code
A guide to code judiciously
- [ ] minimize the human effort needed to create and maintain the required system.
- [ ] When we are coding, we use to spend more time (much more time) reading code than writing

``"Indeed, the ratio of time spent reading versus writing is well over 10 to 1” — Robert C. Martin, Clean Code"
``
# Naming
We are deciding names everywhere when we are coding: variables, functions, classes, packages, files… Taking it seriously is a first step to having Clean Code.

Some tips to get clean names:

Use intention-revealing names:
Use intention-revealing names example
If you find this “s” entity later you get nothing about its purpose
Choose pronounceable names:
Use pronounceable names example
It’s not easy to talk with a colleague about the red variable without losing face
Use searchable names:
Seachable names example
If you try to find the “r” variable with your IDE’s search tool, probably you will find more than you want
Avoid prefixes and suffixes and abbreviations
Avoid abbreviations

# Functions
Between all the ideas about clean functions I am going to highlight three for this post.

First rule is basic and easy to remember: Functions should do one thing, they should do it well and they should do it only. Not too much to explain here: avoid side effects, split your functions if you notice that they are doing several things at the same time.
Functions should do one thing
Functions should be small. Ok, but how short they should be? How to measure it? Let’s force our functions to have no more than 2 levels of indentation. If this is hard for you, you can start setting a higher limit (3 levels, for example), but please put a limit on the levels of indentation you allow.
Regarding the arguments… The fewer arguments a function has, the cleaner it is. Why? Arguments need a lot of context knowledge. In each call a reader must have context to understand each argument. More arguments→ more context you need to understand. Arguments are also hard from a testing point of view. More arguments, more test cases to ensure that all the combinations of arguments work properly
Function classification by the number of arguments. More than 2 not recommended

# Comments
When I learned to code in the 90's, my teachers used to ask me to write comments everywhere. It was typical to hear them say things like “If you don’t comment your code, I’m not going to correct your exam…”. The goal of those comments was to make our code easier to read. This is a goal that we also have when writing Clean Code, but maybe comments are not the best way to achieve it.

``"Comments compensate for our failure to express ourselves in code. Comments are always failures” — Robert C. Martin, Clean Code"
``

I agree with Martin in this point. He also says that comments lie, and I am sure that we have all found old comments saying something outdated. Because the code is maintained, but there is nothing that forces the comments to be maintained as well. Is there anything worse than a fake comment?

The truth is only in the code. When you think you need to write a comment, always think if there is not a better way to express this using the code.

The most important idea is to try to avoid comments to explain the code. For example:

Avoid comments to explain a variable. Instead, choose a good name for this variable and you won’t need a comment
Avoid comments to explain a function. Instead, force your function to do only one thing, have few arguments and choose a good name for it and its arguments and you won’t need a comment

```
Always code as if the person who ends up maintaining your code is a violent psychopath who knows where you live — John F. Woods.
```
