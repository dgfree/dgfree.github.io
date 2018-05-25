---
layout: post
title: Quotient Space Intuition
---
We're going to hang out in a linear algebra setting today. Let's say we have a vector space $V$ and a subspace $W \subset V$. We often see the <u>quotient space</u> $V/W$ defined as the set of all cosets $v + W = \{v + w : w \in W\}$.  Let's get some intuition on what that means.

Let's take our big space to be $V = \mathbb{R}^3$. We could take any subspace of this space, but let's just consider the $xy$-plane, call it $W$.![Screenshot from 2018-05-24 17-53-01](/images/post01/figure1.png) *Figure 1: The $xy$ plane, our $W$, in 3D space.* 

Now let's take a look at what a "coset" is. So, we'll just take some vector in $\mathbb{R}^3$, and we'll call it $v$. 



![Screenshot from 2018-05-24 18-02-59](/images/post01/figure2.png)*Figure 2: Our vector $v$ in red. This one is $\langle 1,-2,3 \rangle$.*

We can think of the coset corresponding to $v$ as the addition of $v$ with *any* possible vector in $W$. Since vectors in $W$ have the form $\langle x,y,0 \rangle$, Then the coset corresponding to our $v$ in this case are the vectors $\langle 1 + x, -2 + y, 3 \rangle$. Since $x, y$ are arbitrary, This is essentially the plane $z=3$ (or, in parametric form, $(u,v,3)$). Let's take a look at what that looks like. 

![Screenshot from 2018-05-24 18-13-35](/images/post01/figure3.png)

Here, we have our vector $v$ in red, a vector $w \in W$ in yellow, and the sum $v + w$ in blue. Imagine picking *every* vector in $W$ and adding it to our $v$. In this case, this creates a plane (shown in green) with the $z$ component the same as $v$ (In this $v$'s case, $z=3$). You can think of this *plane* as a vector in our space $V/W$. Notice that this plane is parallel to our subspace $W$. 

![output](/images/post01/figure4.gif)*Figure 4: We iterate over some vectors in $W$ in yellow and show the sum of $v + w$ in blue. We can see that the blue vectors will always be contained in the plane $z=3$.*

Now. we might notice that if we take any vector $v_0 \in V$ with $z$-component equal to 3, then the coset $v_0+W$ will be the same as the coset we had before, $v+W$.  This leads to the fact of these cosets:

**FACT:** *$v + W = v_0 + W$ if and only if $v-v_0 \in W$.* 

For our case, note than any two vectors in $W$ (the $z=3$ plane) will have z-component $3$. So, if you subtract any two vectors in $v+W$, you will get a $z$ component of $0$. 

Remember, this is plane is just one element of the vector space $V/W$. In general, the space $V/W$ contains all planes parallel to the $xy$-plane. These planes are determined only by their $z$-coordinate, so we might note a couple of things. 

One is that this vector space $V/W$ is essentially just the z-axis. Since any vector in there is only determined by its $z$-component, it is equivalent to vectors that lie on the $z$-axis. 

Then, we can see that the dimension  $\dim V/W = 1$. Indeed, in general we have (assuming our vector spaces are finite dimensional) $\dim V/W = \dim V - \dim W$. 

So, how else can we think of the quotient space? Well, in our example, we are removing the importance of the $x$ and $y$ components of our vectors. Essentially, we are "squishing" them to zero and only looking at the $z$ component of any vectors. Any vectors with the same $z$-component, in this quotient space, are said to be equivalent. So, in a way, we are removing $W$ from our vector space, and only looking at what is left in $V$. 



