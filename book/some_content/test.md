(Sec:Taylor polynomials_WBMT)=
# Taylor polynomials<br>for BSc WB & MT

## Introduction

Additions and multiplications are easy to compute by hand, but if you had to determine the value of $\sqrt[3]{9}$ you would probably need a calculator. The function $\sqrt[3]{x}$, however, can be approximated by polynomials. Polynomials are functions that can be written as sums of multiples of powers of $x$. The functions $1+x-3x^4$ and $-2-5x^2+2x^6-x^7$ are examples of polynomials.


```{math}
\int_{\R^n} \mathbb{1}_A(x)\,\mathrm{d}x.
```

In einem gewissen Sinn sind Maße ein *fundamentaleres Konzept* als das der Integration, da sich jede Integration auf die Berechnung von Maßen stützt.

Eins der berühmtesten Beispiele zur Motivation der Maßtheorie ist im Folgenden erklärt.

````{prf:example} Dirichlet-Funktion
:label: ex:dirichletFunktion

Wir betrachten das kompakte Intervall $[0,1] \subset \R$ und definieren hierauf die sogenannte **Dirichlet-Funktion** $\mathbb{1}_\Q \colon [0,1] \rightarrow \{0,1\}$ mit

```{math}
\mathbb{1}_\Q(x) := \begin{cases} 1, \ \text{ falls } x \in \Q, \\ 0, \ \text{ sonst }.\end{cases}
```

Diese Abbildung kann als *charakteristische Funktion* der rationalen Zahlen $\Q$ aufgefasst werden.
Man sieht leicht ein, dass diese Funktion **nicht Riemann-integrierbar** ist, da alle Untersummen stets $0$ und alle Obersummen stets $1$ sind.
````

## Taylor polynomials

Function values of polynomials are easy to find since you only need to be able to add and multiply numbers. This means that we can use these polynomials to obtain a good guess of what $\sqrt[3]{9}$ should more or less be equal to. In this text we will show you how you can approximate functions by polynomials and apply them to solve various problems.

**Approximation by a linear function**

We already saw how we can use a _linear function_ to approximate a function $f$. The linearization of $f$ at a point $a$ was given by the formula

$$L(x)=f(a)+f'(a)(x-a).$$

You can check yourself that $L(x)$ is a polynomial of degree one that has, at the point $a$, the same value and the same derivative as $f(x)$. From now on, we will also refer to the linearization $L(x)$ of $f$ at $x=a$ as the Taylor polynomial $T_1(x)$ of degree one of $f$ centered at $x=a$. By definition, the graph of $T_1$ is the tangent line to the graph of $f$ at the point $(a,f(a))$, so it makes sense to state that $f(x)\approx T_1(x)$ for all $x$ that are close to $a$. By the expression $f(x)\approx T_1(x)$, we mean that $T_1(x)$ is an approximation of $f(x)$.

::::{prf:example}
:label: Ex:TaylorPolynomials:cuberootWBMT

Let's use the function $f(x)=\sqrt[3] x$ as an example and say that $a=8$. Since $f(8)=2$ and $f'(8)  =  \frac{1}{12}$, we have

$$
T_1(x) \ = \ 2+\frac{1}{12}(x-8).
$$

This leads to the approximation

$$
\sqrt[3] x \ \approx \  2+\frac{1}{12}(x-8).
$$

{numref}`Figure %s <Fig:TaylorPolynomials:cuberootWBMT>` shows the graph of $\sqrt[3]{x}$ and the Taylor polynomial $T_1(x)$.

:::{figure} Images/Fig-TaylorPolynomials-cuberoot.svg
:name: Fig:TaylorPolynomials:cuberootWBMT
:class: dark-light

The function $\sqrt[3]{x}$ and the Taylor polynomial $ T_1(x)$.

:::

You can clearly see that for any $x$ close to $8$ the values of $f(x)$ and $T_1(x)$ are very close to each other.

Let us use this observation to _approximate_ $\sqrt[3]{9}$:

$$
\sqrt[3]{9} = f(9) \approx T_1(9) = 2+\frac{1}{12}(9-8) = 2+\frac{1}{12} = \frac{25}{12} = 2.08\overline{33}.
$$

::::

**Approximation by a quadratic function**

We can now ask ourselves whether is possible to find a _quadratic function_ $T_2$ such that $T_2(a)=f(a)$, $T_2'(a)=f'(a)$ and $T_2''(a)=f''(a)$, in other words $T_2^{(k)}(a)=f^{(k)}(a)$ for $k=0,1,2$. A straightforward verification shows that these requirements are met by the function

$$
T_2(x)=f(a)+f'(a)(x-a)+\frac 12 f''(a)(x-a)^2.
$$

This function will be called the _Taylor polynomial of order 2 centered at_ $x=a$.

::::{prf:example}
:label: Ex:TaylorPolynomials:cuberoot-quadWBMT

Let's see how this works out for our function $f(x)=\sqrt[3] x$ when $a=8$. Since $f(8)=2$, $f'(8)=\dfrac{1}{12}$ and $f''(8)=-\dfrac{1}{144}$, we have

$$
T_2(x) \ = \ 2+\frac 1{12}(x-8)-\frac 1{288}(x-8)^2.
$$

This leads to the approximation

$$
\sqrt[3] x \ \approx \ 2+\frac 1{12}(x-8)-\frac 1{288}(x-8)^2.
$$

In {numref}`Figure %s <Fig:TaylorPolynomials:cuberootquadWBMT>` you can see that this quadratic polynomial is indeed a better approximation than the linearization. 

:::{figure} Images/Fig-TaylorPolynomials-cuberoot-quad.svg
:name: Fig:TaylorPolynomials:cuberootquadWBMT
:class: dark-light

The function $\sqrt[3]{x}$ and the Taylor polynomials $T_1(x)$ and $T_2(x)$.

:::

Let us use this observation to _approximate_ $\sqrt[3]{9}$:

$$
\sqrt[3]{9} = f(9) \approx T_2(9) = 2+\frac{1}{12}(9-8)-\frac 1{288}(9-8)^2 = 2+\frac{1}{12}-\frac 1{288} = \frac{599}{288} = 2.07986\overline{11}.
$$

::::

Now, we can generalize this idea to Taylor polynomials of order $n$.

**Higher order approximations**

Continuing this process, we define the Taylor polynomial of order three as

$$
T_3(x) \ = \ f(a)+f'(a)(x-a)+\frac 12f''(a)(x-a)^2+\frac 16f'''(a)(x-a)^3.
$$

The Taylor polynomial $T_n(x)$ of degree $n$ of a function $f(x)$ centered at $a$ will be defined as

::::{prf:definition} 

The **$n$th-order Taylor polynomial $T_n$ of $f$ with center $a$** is given by 

:::{math} 
:label: Eq:TaylorPolynomials:TnWBMT

T_n(x)= f(a)+f'(a)(x-a)+\frac {f''(a)}{2} (x-a)^2+\frac {f'''(a)}{3!} (x-a)^3+ \ \cdots \ +\dfrac {f^{(n)}(a)}{n!}(x-a)^n,

:::

where

$$
k! = 1 \cdot 2 \cdot 3 \cdot \ldots \cdot k
$$

for integers $k\geq1$ and $0!=1$.

::::

Using the summation sign notation, Equation {eq}`Eq:TaylorPolynomials:TnWBMT` can be written as follows:

$$
T_n(x)=\sum_{k=0}^n \frac{f^{(k)}(a)}{k!}(x-a)^k.
$$

These functions can be used to approximate $f(x)$ if $x$ is not too far from $a$.

::::{prf:example}
:label: Ex:TaylorPolynomials:expWBMT

Taylor polynomials of $e^x$ centered at $0$ are easy to compute since this function is its own derivative. This implies that if $f(x)=e^x$, then $f^{(n)}(0)$ is equal to $1$ for each $n$. If we plug this into the formula for $T_3(x)$, then we find the following polynomial:

$$
1+x+\frac{1}{2}x^2+\frac{1}{6}x^3.
$$

In fact, the Taylor polynomial of order $n$ centered at $0$ of the function $e^x$ is equal to

$$
1+x+\frac{1}{2}x^2+\frac{1}{6}x^3+ \cdots +\frac{1}{n!}x^n.
$$

::::

::::{prf:example}
:label: Ex:TaylorPolynomials:cosWBMT

Computing Taylor polynomials of $\cos(x)$ requires a little bit more work. Let's start with an approximation by a second-order Taylor polynomial centered at 0. The derivative of $\cos(x)$ is $-\sin(x)$ and the second derivative is equal to $-\cos(x)$. For $f(x)=\cos(x)$ we therefore have $f(0)=1$, $f'(0)=0$ and $f''(0)=-1$. The Taylor polynomial $T_2(x)$ is equal to

$$
1-\frac{1}{2}x^2.
$$

If we want to find $T_3(x)$ we also need the third derivative of $\cos(x)$, which is equal to $\sin(x)$. Because $\sin(0)=0$, we do not get an extra term of degree three in the Taylor polynomial $T_3(x)$. This means $T_3(x)$ is equal to $T_2(x)$. We do get an extra term if we compute the Taylor polynomial of order $4$. We have $f^{(4)}(0)=\cos(0)=1$, so

$$
T_4(x)=1-\frac{1}{2}x^2+\frac{1}{24}x^4.
$$

::::

## Taylor's inequality

So far we have been saying that Taylor polynomials provide us with a way to approximate functions, but how good are these approximations? Is $2$ a good approximation of the number $\sqrt[3]{9}$ or is $2.0801$?

::::{prf:example}
:label: Ex:TaylorPolynomialsAdd:cuberootWBMT

Let's use the Taylor polynomials of the function $f(x)=\sqrt[3]{x}$ that we already computed to find an approximation of $\sqrt[3]{9}$. The first order Taylor polynomial centred at $8$ is equal to

$$
T_1(x)=2+\frac{1}{12}(x-8).
$$

What do we obtain when we use it to approximate $\sqrt[3]{9}$?

$$
\sqrt[3]{\textcolor{red}{9}} = f(\textcolor{red}{9}) \ \approx T_1(\textcolor{red}{9}) =  \ 2+\frac{1}{12}(\textcolor{red}{9}-8) \ = \ \frac{25}{12} \ = \ 2.0833\ldots.
$$

How accurate is this approximation? The actual value of $\sqrt[3]{9}$ is $2.0801\ldots$. This means that the approximation error is in this case equal to:

$$
|f(9) - T_1(9)| = |\sqrt[3]{9}-\frac{25}{12}| =|2.0801\ldots - 2.0833\ldots|= 0.0032\ldots.
$$

If we use a second-order Taylor polynomial we will get a better approximation. Remember that the second-order Taylor polynomial of $\sqrt[3]{x}$ centered at $x=8$ is equal to

$$
T_2(x)=2+\frac{1}{12}(x-8)-\frac{1}{288}(x-8)^2.
$$

This gives us the following approximation of $\sqrt[3]{9}$:

$$
T_2(\textcolor{red}{9}) = 2+\frac{1}{12}(\textcolor{red}{9}-8)-\frac{1}{288}(\textcolor{red}{9}-8)^2 \ = \  \frac{599}{288} \ = \ 2.0798\ldots.
$$

For this approximation the error is equal to

$$
|f(9) - T_2(9)| = |\sqrt[3]{9}-\frac{599}{288}| =|2.0801\ldots - 2.0798|\ldots= 0.0003\ldots.
$$

Next we will show how you can determine an upper bound for these approximation errors.

::::

We would like to be able to have an upper bound for the difference between the approximation of a certain value and the actual value. To do so, we first give two examples.

::::{prf:example}
:label: Ex:TaylorPolynomialsIneq:speed1WBMT

Consider we have a scooter:

:::{figure} Images/scooter.jpg
:name: Fig:TaylorPolynomials:cuberoot-quadWBMT
:figwidth: 50%

A scooter. <a href="https://www.vecteezy.com/free-vector/scooter">Scooter Vectors by Vecteezy</a>

:::

Let's assume that this scooter has

- position $x(0)=5\,\mathrm{m}$ at $t=0\,\mathrm{s}$;

- velocity $v(t)=10\,\dfrac{\mathrm{m}}{\mathrm{s}}$ for all $t$.

Using this information we can determine the position of the scooter after $10$ seconds, as in $10$ seconds the scooter will have traveled $10\,\mathrm{s}\cdot10\,\dfrac{\mathrm{m}}{\mathrm{s}}=100\,\mathrm{m}$, so $x(10)=x(0)+100\,\mathrm{m}=105\,\mathrm{m}$.

::::

::::{prf:example}
:label: Ex:TaylorPolynomialsIneq:speed2WBMT

Consider we have the same scooter, but now assume that this scooter has

- position $x(0)=5\,\mathrm{m}$ at $t=0\,\mathrm{s}$;

- velocity $v(0)=10\,\dfrac{\mathrm{m}}{\mathrm{s}}$  at $t=0\,\mathrm{s}$;

- acceleration $a(t)$ with $0\,\dfrac{\mathrm{m}}{\mathrm{s}^2}\leq a(t)\leq 0.1\,\dfrac{\mathrm{m}}{\mathrm{s}^2}$ for all $t$.

Using this information we cannot determine the position of the scooter after $10$ seconds _exactly_, as we do not know the _exact_ velocity of the scooter in those 10 seconds.

What we can do, is _estimate_ the position after $10$ seconds.

To do this, we consider the information we have on the acceleration: it is at _minimum_ $0\,\dfrac{\mathrm{m}}{\mathrm{s}^2}$ during those 10 seconds. If we assume the acceleration equals $0\,\dfrac{\mathrm{m}}{\mathrm{s}^2}$ during those 10 seconds, the velocity will be the lowest during the time frame, which also indicates the least distance traveled by the scooter. So in this case, the velocity will remain $10\,\dfrac{\mathrm{m}}{\mathrm{s}}$ and the distance traveled will be again $100\,\mathrm{m}$. So at _minimum_ the scooter will have position $105\,\mathrm{m}$, or in symbols:

$$
x(10) \ge 105.
$$

Now we focus on the _maximum_ acceleration, which is $0.1\,\dfrac{\mathrm{m}}{\mathrm{s}^2}$. If we assume the acceleration equals $0.1\,\dfrac{\mathrm{m}}{\mathrm{s}^2}$ during those 10 seconds, the velocity will be the highest during the time frame, which also indicates the most distance traveled by the scooter. In this case this means that the velocity increases linearly from $10\,\dfrac{\mathrm{m}}{\mathrm{s}}$ to $10\,\dfrac{\mathrm{m}}{\mathrm{s}}+0.1\,\dfrac{\mathrm{m}}{\mathrm{s}^2}\cdot10\,\mathrm{s}=11\,\dfrac{\mathrm{m}}{\mathrm{s}^2}$ in $10$ seconds. In formula form:

$$
v(t)=10+0.1\cdot t.
$$

Now we know this, we can also estimate the _maximum_ position after $10$ seconds:

$$
x(10) \leq x(0) + \int_{0}^{10}v(t)\,dt = 5 + \int_0^{10}10+0.1\cdot t\,dt = 5 + \left[5\left(10+0.1\cdot t\right)^2\right]_{t=0}^{10} = 5 + \left(605 - 500\right) = 110.
$$

In conclusion, we found that the position of the scooter after $10$ seconds satisfies

$$
105 \le x(10) \le 110,
$$

where we used information about the velocity, i.e. the _first derivative_ of the position, at one time moment and bounds for the acceleration, i.e. the _second derivative_ of the position.

::::

In the above example we could say that we approximated the position after $10$ seconds using a _first order_ Taylor polynomial $T_1(x)=x(0)+v(0)\cdot t$ and that we found an interval for the exact value using bounds on  the _second derivative_.

The next theorem generalises the above examples and gives us the tools to always find an upper bound for the difference between the _exact_ value and an _approximation_ using Taylor polynomials:

::::{prf:theorem}

Define $D$ as an interval that contains the point $a$, $T_n$ as the $n$<sup>th</sup> order Taytlor polynomial of $f$ around $a$ and $M$ as an upper bound for $|f^{(n+1)}(x)|$ on the interval $D$. Then

:::{math}
:label: Ex:TaylorPolynomialsAdd:TaylorIneqWBMT

|f(x)-T_n(x)|\leq \dfrac{M |x-a|^{n+1}}{(n+1)!}

:::

for all $x$ in $D$.

::::

This theorem can be visualed as in {numref}`Figure %s <Fig:TaylorPolynomials:errorWBMT>`, where we use $n=1$.

:::{figure} Images/Fig-TaylorPolynomials-error.svg
:name: Fig:TaylorPolynomials:errorWBMT
:figwidth: 50%
:class: dark-light

Suppose $|f''(x)|\leq M$ for all $x$, then $T_1(x)-\frac{M}{2}x^2\leq f(x)\leq T_1(x)+\frac{M}{2}x^2$.

:::


To make talking about these formulae a little easier, we name parts of it:

::::{prf:definition}

The Inequality {eq}`Ex:TaylorPolynomialsAdd:TaylorIneqWBMT` is called **Taylor's inequality**.

The expression $f(x)-T_n(x)$ is called the **remainder** $R_n(x)$.

The absolute value of the remainder, $E_n=|R_n(x)|=|f(x)-T_n(x)|$ is the **approximation error**.

::::

The next example shows how you can determine an upper bound for the approximation error.

::::{prf:example}
:label: Ex:TaylorPolynomialsAdd:cos4WBMT

Let's construct an approximation of $\cos(0.5)$ by using the fourth-order Taylor polynomial $T_4$ of the cosine function $f(x)=\cos(x)$ centered at $x=0$:

$$
T_4(x) \ = \ 1-\frac{1}{2}x^2+\frac{1}{24}x^4.
$$

The approximation that we find is

$$\cos(\textcolor{red}{0.5})=f(\textcolor{red}{0.5}) \ \approx T_4(\textcolor{red}{0.5}) \ 1-\frac{1}{2}\left(\textcolor{red}{0.5}\right)^2+\frac{1}{24}\left(\textcolor{red}{0.5}\right)^4 \ = \ 0.877604\ldots.$$

In order to find an upper bound for the approximation error we will need to find an $M$ such that the fifth derivative $f^{(5)}$ of the cosine function is smaller than $M$ for all numbers $x$ in the interval $[0, 0.5]$. The fifth derivative of $f(x)=\cos(x)$ is equal to $f^{(5)}(x)=-\sin(x)$. We know that $|-\sin(x)|\leq 1$ for all values of $x$, so we can choose $M$ to be equal to $1$. We get the following upper bound for the remainder:

$$
\begin{align*}
\left|R_4\left(\textcolor{red}{0.5}\right)\right| &= |f(\textcolor{red}{0.5})-T_4(\textcolor{red}{0.5})| \\
&\leq \frac{1\cdot |\textcolor{red}{0.5}-0|^{4+1}}{(4+1)!} \\
&= \frac{(0.5)^{5}}{5!} \\
&= \frac{0.03125}{120} \\
&= 0.00026\ldots.
\end{align*}
$$

Thus, the approximation error is at most $0.00027$, as we must round up to ensure a proper upper bound.

Now we have an upper bound for the _absolute_ value of the error, we can even find an interval in between the _exact_ value of $\cos(0.5)$ lies:

$$
\begin{array}{rcl}
& |f({0.5})-T_4({0.5})| & \leq 0.00027 \\
-0.00027 \le  & \cos({0.5})- 0.877604 & \leq 0.00027 \\
0.877604-0.00027 \le & \cos({0.5}) &\leq 0.877604+0.00027 \\
0.877334 \le & \cos({0.5}) &\leq 0.877874 \\
\end{array}
$$

::::

Most of the time when we are looking for an approximation we want to find a value that lies within a given margin of error. The next example shows exactly how we can do that.

::::{prf:example}
:label: Ex:TaylorPolynomialsAdd:sinWBMT

Suppose that we want to find an approximation of $\sin(0.8)$ such that the difference between the approximation and the actual value is at most $0.0001$. We will use a Taylor polynomial of the function $f(x)=\sin(x)$ and evaluate it in $x=0.8$. What order Taylor polynomial do we need to use?

The derivatives of the sine function $f(x)=\sin(x)$ are all equal to either $\cos(x)$, $-\sin(x)$, $-\cos(x)$ or $\sin(x)$. This means that for each $n$ and for each $x$ we have $|f^{(n+1)}(x)|\leq 1$. Therefore we know that

$$
\left|R_n\left(0.8\right)\right|\leq \frac{(0.8)^{n+1}}{(n+1)!}.
$$

Using this formula, we can make a table with in each row a different value of $n$ and the corresponding upper bound:

:::{table}
:class: longtable table-bordered table-striped table-hover table

|$n$|$\|R_n(0.8)\|\leq$|
|-|-|
|$0$|$0.8$|
|$1$|$0.32$|
|$2$|$0.085\overline{33}$|
|$3$|$0.0170\overline{66}$|
|$4$|$0.002730\overline{66}$|
|$5$|$0.0003640\overline{88}$|
|$6$|$0.00004161\overline{015873}$|
|$7$|$0.000004161\overline{015873}$|

:::

For $n=3$ the right-hand side of the inequality is $0.0170\overline{66}$. This value is not smaller than 0.0001 and thus a Taylor polynomial of order three may not be sufficient to give us an approximation that is good enough. If $n$  is equal to 4 we obtain that the approximation error is smaller than $0.002730\overline{66}$. After a little trial and error we find that for $n=6$ the error is smaller than $0.00004161\overline{015873}$ and therefore also smaller than $0.0001$. A Taylor polynomial of order 6 will give us the approximation that we want. For the sine function this polynomial is equal to

$$
T_6(x)=x-\frac{1}{6}x^3+\frac{1}{120}x^5.
$$

There is no term of degree six since the sixth derivative of $\sin(x)$ is zero in $x=0$. The approximation that we find is

$$
T_6\left( \textcolor{red}{0.8} \right) \ = \ \textcolor{red}{0.8}-\frac{1}{6}\left( \textcolor{red}{0.8} \right)^3+\frac{1}{120}\left( \textcolor{red}{0.8} \right)^5 \ = \ 0.717397\ldots.
$$

Since the error is smaller than 0.0001 this means that the actual value of $\sin(0.8)$ lies in between $0.7172$ and $0.7175$.

::::

## Exercises



::::::{exercise}
:label: Exc:TaylorPolynomials:firstexWBMT

Determine the Taylor polynomial of order three for the given function centered at the given $a$.

<ol type="a">

<li>

$\sqrt{x} \quad\text{with}\quad a=4$

</li>

<li>

$\arctan{x} \quad\text{with}\quad a=0$

</li>

<li>

$\ln{x} \quad\text{with}\quad a=1$

</li>

<li>

$\dfrac{1}{1+x} \quad\text{with}\quad a=0$

</li>

</ol>

::::::

::::::{exercise}
:label: Exc:TaylorPolynomials:error1WBMT

Determine a Taylor polynomial of order two centered at $a$ and show that the approximation error is less than 0.001 on the given interval:

<ol type="a">

<li>

$e^x,\quad a=0,\quad-0.1\leq x \leq 0.1$;

</li>

<li>

$\dfrac{1}{x^2},\quad a=1,\quad0.95\leq x \leq 1.05$;

</li>

<li>

$\sqrt{x},\quad a=4,\quad3.5\leq x \leq 4.5$.

</li>

</ol>

::::::

::::{exercise}
:label: Exc:TaylorPolynomials:error2WBMT

Use Taylor polynomials of order $n$ centered at 0 in exercises 8 to 11 to approximate the given value and show that the approximation error is smaller than $\epsilon$:

<ol type="a">

<li>

$\cos(0.3),\quad n=2,\quad \epsilon=0.01$;

</li>

<li>

$\sin(0.8),\quad n=3,\quad \epsilon=0.02$;

</li>

<li>

$\sqrt[6]{e},\quad n=3,\quad \epsilon=0.001$;

</li>

<li>

$\ln(1.2),\quad n=2,\quad \epsilon=0.01$.

</li>

</ol>

::::

## Solutions



::::{admonition} Solution to&nbsp;{numref}`Exc:TaylorPolynomials:firstexWBMT`
:class: solution, dropdown

<ol type="a">

<li>

$T_3(x)=2+\frac{1}{4}(x-4)-\frac{1}{64}(x-4)^2+\frac{1}{512}(x-4)^3$

</li>

<li>

$T_3(x)= x-\frac{1}{3}x^3$

</li>

<li>

$T_3(x)=(x-1)-\frac{1}{2}(x-1)^2+\frac{1}{3}(x-1)^3$

 </li>

 <li>

 $T_3(x)= 1-x+x^2-x^3$

 </li>

</ol>

::::

::::{admonition} Solution to&nbsp;{numref}`Exc:TaylorPolynomials:error1WBMT`
:class: solution, dropdown

<ol type="a">

<li>

$T_2(x)=1+x+\frac{1}{2}x^2$

$|R_2(x)|\leq \frac{e^{0.1}}{3!} 0.1^3 \leq \frac{e}{3!} 0.1^3 \leq \frac{3}{3!} 10^{-3} = 0.0005<0.001$;

</li>

<li>

$T_2(x)=1-2(x-1)+3(x-1)^2$

$|R_2(x)|\leq \frac{24}{3! 0.95^5} |x-1|^3 \leq \frac{24}{3! 0.95^5} 0.05^3 = 0.00065<0.001$;

</li>

<li>

$T_2(x)=2-2\frac{1}{4}(x-4)-\frac{1}{64}(x-4)^2$

$|R_2(x)|\leq \frac{3}{8} 3.5^{-2.5} \cdot \frac{0.5^3}{3!} = 0.00034<0.001$.

</li>


</ol>

::::

::::{admonition} Solution to&nbsp;{numref}`Exc:TaylorPolynomials:error2WBMT`
:class: solution, dropdown

<ol type="a">

<li>

Given $f(x) = \cos x$ and $a=0$, $T_2(x)=1-\frac{1}{2}x^2$, thus $T_2(0.3)=0.955$.

The interval $D$ we consider here is $0\leq x \leq 0.3$ and $f^{(3)}(x)=\sin(x)$ for which it holds that $|f^{(3)}(x)|<1$. Therefore, $|R_2(x)|\leq \frac{1}{3!} |x|^3 \leq \frac{1}{3!} 0.3^3 = 0.0045<0.01$.

Notice that, since $f^{(3)}(0)=0$, $T_2(x)=T_3(x)$ and therefore $|R_3(x)|\leq \frac{1}{4!} |x|^4 \leq \frac{1}{4!} 0.3^4 = 0.00034$.

</li>

<li>

Given $f(x) = \sin x$ and $a=0$, $T_3(x)=x-\frac{1}{6}x^3$, thus $T_3(0.8)=0.71467$.

The interval $D$ we consider here is $0\leq x \leq 0.8$ and $f^{(4)}(x)=\sin(x)$ for which it holds that $|f^{(4)}(x)|<1$. Therefore, $|R_3(x)|\leq \frac{1}{4!} |x|^4 \leq \frac{1}{4!} 0.8^4 = 0.017<0.02$.

Notice that, since $f^{(4)}(0)=0$, $T_3(x)=T_4(x)$ and therefore $|R_4(x)|\leq \frac{1}{5!} |x|^5 \leq \frac{1}{5!} 0.3^5 = 0.00273$.

</li>

<li>

Given $f(x) = e^x$ and $a=0$, $T_3(x)=1+x+\frac{1}{2}x^2+\frac{1}{6}x^3$, thus $T_3(\frac{1}{6})=1.22133$.

The interval $D$ we consider here is $0\leq x \leq \frac{1}{6}$ and $f^{(4)}(x)=e^x$ for which it holds that $|f^{(4)}(x)|<e^{\frac{1}{6}}$ on $D$. Therefore, $|R_3(x)|\leq \frac{e^{\frac{1}{6}}}{4!} |x|^4 \leq \frac{e^{\frac{1}{6}}}{4!} (\frac{1}{6})^4 \leq 0.0001$.

</li>

<li>

Given $f(x) = \ln (1+x)$ and $a=0$, $T_2(x)=x-\frac{1}{2}x^2$, thus $\ln(1.2)=f(0.2)\approx T_2(0.2)=0.18$.

The interval $D$ we consider here is $0\leq x \leq 0.2$ and $f^{(3)}(x)=\frac{2}{(1+x)^3}$ for which it holds that $|f^{(3)}(x)|<2$ on $D$. Therefore, $|R_2(x)|\leq \frac{2}{3!} |x|^3 \leq \frac{2}{3!} (0.2)^3 \leq 0.00267<0.01$.

</li>


</ol>

::::
