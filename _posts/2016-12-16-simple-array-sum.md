---
layout: post
title: "Simple Array Sum"
date: 2016-12-15
comments: true
categories: algorithms warmup
hackerrank: https://www.hackerrank.com/challenges/simple-array-sum
youtube: YFaVWvUbKTk
---
For our next challenge, we'll be finding the sum of a list of numbers.

We're given two lines of inputs, the first line tells us how many numbers there are, and the next line has that many numbers. Our goal is to sum the numbers in the second line.

Sample input:
{% highlight java %}
4
3 2 6 4
{% endhighlight %}

Sample output:
{% highlight java %}
15 // 3 + 2 + 6 + 4 = 15
{% endhighlight %}

First, let's set up our code to read from the standard input.
{% highlight java %}
import java.util.*; //so we can use our Scanner

public class Solution {
    public static void main(String[] args){
        Scanner in = new Scanner(System.in);
        //more code
    }
}
{% endhighlight %}

In the `//more code` section, we can read the first integer, which gives us the number of items to sum up.
{% highlight java %}
int n = in.nextInt();
{% endhighlight %}

Let's also have another variable called `sum` to keep track of our total sum as we read in the next `n` integers.
{% highlight java %}
int sum = 0;
{% endhighlight %}

To add the numbers together, let's use a `for` loop. For an explanation on what a `for` loop is, check the above video at around the **1:57** mark.

The final code looks something like this:
{% highlight java %}
import java.util.*;

public class Solution {
    public static void main(String[] args){
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int sum = 0; 

        for(int i = 0; i < n; i++){
            sum += in.nextInt();
        }

        System.out.println(sum);
    }
}
{% endhighlight %}

`sum += in.nextInt()` means to store the result of the addition `sum + in.nextInt()` back into `sum`.
