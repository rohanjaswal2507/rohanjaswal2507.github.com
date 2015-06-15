---
layout: post
title: "Generate all the Prime numbers between two large numbers"
description: "This blog post is a tutorial to find all the prime numbers between any two large integers"
category: Algorithms 
tags: [Sieve of Eratosthenes, Prime numbers ]
---
{% include JB/setup %}

Problems dealing with prime numbers have always been of great interest to the programmers.
One of the such problems is to generate all the prime numbers between any two Integers.
The problems is very popular and finds its place in all the programming sites.

###Problem Statement
You have to generate all the **prime numbers** between two given integers **x** and **y**.

####Constraints:

**x** < **y** <= 1000000000

**y** - **x** < 100000


So, the range of the numbers is quite large.
Using the standard algorithms like **Sieves** won't be a nice idea.
The best solution to this problem is to use **Sieve fo Eratosthenes** with little modification to make that work for large numbers.

First of all, We will find and store all the prime numbers upto **31622**.
31622 is the nearest integer to sqrt of 10^9.

To do this, We will use the following approach. I have intitialised an array with all the prime numbers upto **177**(sqrt(31622) = 177.82).

{% highlight c %}
// Prime Number upto sqrt(31622)
int a[39] = {2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97,101,103,107,109,113,127,137,139,149,151,157,163,167,173};
{% endhighlight %}

After this, We will find out all the prime number upto 31622.
To do that, We will apply Sieve of Eratosthenes for numbers upto 31622.

{% highlight c %}
//find prime numbers upto 31623 i.e. sqrt(1000000000)
for ( i = 0; i < 39; i++ ) {
    m = 2*a[i];
    while ( m < 31623 ) {
        b[m] = 1;   //set all multiples of a[i] to 1
        m = m + a[i];
    }
}
{% endhighlight %}

Let's store all the prime numbers in an array **prime**.

{% highlight c %}
for ( i = 2; i < 31623; i++ ) {
    if ( b[i] == 0 )
    prime[prime_count++] = i;
}
{% endhighlight %}

The real magic will happen now. (Here, `upper` is **y** and `lower` is **x**).

{% highlight c %}
for ( i = 0; i < prime_count; i++ ) {
    if ( upper > prime[i] ) {
        q = (double) lower/prime[i];
        k = ceil (q);
    
    	if ( k == 1 )
		    m = prime[i] * 2 - lower;
    	else
    	    m = prime[i] * k - lower;

    	while ( m < diff ) {
    	    r[m] = 1;
    	    m += prime[i];
    	}
    }
}
{% endhighlight %}
Let us crack down the above code.

We will eliminate all the numbers from our list(given range) which are divisible by any of the prime numbers upto 31622.

So, for all the prime numbers, We will eliminate their multiples from the given range.
For example, if the prime number is 31, we will eliminate the numbers 62, 93, 124 and so on.

`m = prime[i] * 2 - lower` finds the first number which is a multiple of `prime[i]` in the given range.
Actually, `lower + m` is the first number which is a multiple of `prime[i]`.


Then, all the numbers in the given range are eliminated using the `while ( m < diff )` loop.
So, the numbers `lower + m`, `lower + m + p[i]`, `lower + m + 2p[i]` and so on are deleted.
In the end, we are left those numbers which are not divisible by any of the integers.

A `for` loop can be used in this way to print the required numbers.
{% highlight c %}
for ( i = 0; i < diff; i++ ) {
	if ( r[i] == 0 ) {
    	printf ( "%ld ", lower+i );
    }
}
{% endhighlight %}


Here is the full source code of the solution written in C.
{% highlight c %}
#include <stdio.h>
#include <math.h>

// Prime Number upto sqrt(31623)
int a[39] = {2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97,101,103,107,109,113,127,137,139,149,151,157,163,167,173};


int b[31623] = {0};
int prime_count = 0;
int prime[31622];

int main () {
    int i, size, k, m, diff;
    long int lower, upper;
    double q;
    int r[100000] = {0};
    b[0] = b[1] = 1;

    //find prime numbers upto 31623 i.e. sqrt(1000000000)
    for ( i = 0; i < 39; i++ ) {
        m = 2*a[i];
        while ( m < 31623 ) {
            b[m] = 1;   //set all multiples of a[i] to 1
            m = m + a[i];
        }
    }

    for ( i = 2; i < 31623; i++ ) {
        if ( b[i] == 0 )
            prime[prime_count++] = i;
    }

    scanf ( "%ld%ld", &lower, &upper);  //Input values
    diff = upper - lower + 1;
    
    for ( i = 0; i < diff; i++ ) {
        r[i] = 0;
    }
    if ( lower == 1 ) 
        r[0] = 1;

    for ( i = 0; i < prime_count; i++ ) {
        if ( upper > prime[i] ) {
            q = (double) lower/prime[i];
            k = ceil (q);
        }
        if ( k == 1 )
            m = prime[i] * 2 - lower;
        else
            m = prime[i] * k - lower;

        while ( m < diff ) {
            r[m] = 1;
            m += prime[i];
        }
    }

    for ( i = 0; i < diff; i++ ) {
        printf ("The prime numbers are:\n");
        if ( r[i] == 0 ) {
            printf ( "%ld ", lower+i );
        }
    }
    printf ("\n");
    return 0;
}
{% endhighlight %}


Any **Comments** or **suggestions** are welcome!





