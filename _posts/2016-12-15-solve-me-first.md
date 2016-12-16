---
layout: post
title: "Solve Me First"
date: 2016-12-15
comments: true
categories: algorithms warmup
hackerrank: https://www.hackerrank.com/challenges/solve-me-first
youtube: bG8YEJx-b-s
---
Let's get started on the first challenge!

We will be given two integer inputs, and our code has to print the sum of the two integers.

Sample input:
{% highlight java %}
2
3
{% endhighlight %}

Sample output:
{% highlight java %}
5
{% endhighlight %}

The template Java code HackerRank has put on right now has a useful hint `//Hint: Type return a+b; below`, but other than that they don't explain very much, so we'll start from scratch instead. Delete all the template code!

First let's make a class. 
{% highlight java %}
public class Solution {
}
{% endhighlight %}

A class is like a blueprint for an object. In this case, a blueprint for our solution. Classes are very important, but in the case of these challenges, (where solutions are written entirely within one file) we don't really need to know much about them other than the fact that we have to write our solutions in a class called `Solution`.

Next, we have to create an entry point for our code to start, this is called `main` and it'll look something like this:
{% highlight java %}
public class Solution {
    public static void main(String[] args){
    }
}
{% endhighlight %}

Now that we've got that down, we need to actually read the integers as they come into our code. To do that, we need the help of a scanner. Instead of writing our own scanner, we'll use [Java's scanner][scanner]. 
In order to use it, we'll have to import it first like so:
{% highlight java %}
import java.util.*;

public class Solution {
    // rest of the code
{% endhighlight %}

Why `java.util.*`? Because when we looked up the [scanner][scanner], above `Class Scanner`, we can see `java.util`. This means that it's in the java util package. The `*` just means to import everything that belongs in the package, which will include the scanner that we need.

To use it, we must first create one:
{% highlight java %}
public static void main(String[] args){
    Scanner in = new Scanner(System.in);
}
{% endhighlight %}

So now we've created a new scanner called `in` for input, and we've also told it that we need it to scan `System.in`. `System.in` is our standard input stream in Java, in other words, where our input will come in.

Now that we have this scanner, we can ask it to do work for us by telling it to read something, in this case, we need it to read the `nextInt()`, and store it in a variable.

{% highlight java %}
public static void main(String[] args){
    Scanner in = new Scanner(System.in);
    int a = in.nextInt();
    int b = in.nextInt();
}
{% endhighlight %}

Using our sample input above with `2` and `3`, our variables `a` will now hold `2` and `b` will hold `3`. The challenge asks us to print the sum of the two integers `a+b`. In order to print, we'll have to tell the system to output a new line to the standard output stream. This is what the completed code will look like:
{% highlight java %}
import java.util.*;

public class Solution {
    public static void main(String[] args){
        Scanner in = new Scanner(System.in);
        int a = in.nextInt();
        int b = in.nextInt();
        System.out.println(a + b);
    }
}
{% endhighlight %}

And that's it! A bit more work then just copying `return a+b;` but I hope it makes more sense.

[challenge]: https://www.hackerrank.com/challenges/solve-me-first
[scanner]: http://docs.oracle.com/javase/1.5.0/docs/api/java/util/Scanner.html
