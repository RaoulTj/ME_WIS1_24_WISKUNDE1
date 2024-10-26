# 2.4 Uitwerkingen

## Opgaven 2.1a

```{admonition} Uitwerkingen
:class: dropdown

%Bepaal analytisch de algemene oplossing van de volgende differentiaalvergelijkigen.

\begin{align*}
y\dfrac{dy}{dx} = x
\end{align*}

Aan beide kanten de integraal nemen naar $dx$.
\begin{align}
 \int y\dfrac{dy}{dx} dx &= \int x dx
\end{align}

De integraal $\dfrac{dy}{dx}dx$ vereenvoudigen tot $dy$.
\begin{align}
 \int y dy &= \int x dx
\end{align}

De primitieven nemen van beide kanten.
\begin{align}
 \frac{1}{2}y^2 + C_1&= \frac{1}{2}x^2 + C_2\\
 y^2 &= x^2 + C_3\\
 y &= \pm \sqrt{x^2 + C} \qquad \text{met } C \in \mathbb{R}
\end{align}
```

## Opgaven 2.1b

```{admonition} Uitwerkingen
:class: dropdown

\begin{align*}
 e^{-x}y^2\dfrac{dy}{dx} = 1
\end{align*}

Alle variabelen met een $y$ naar links en variabelen met een $x$ naar rechts.
\begin{align}
 y^2\dfrac{dy}{dx} &= \frac{1}{e^{-x}}\\
 y^2\dfrac{dy}{dx} &= e^{x}
\end{align}

Aan beide kanten de integraal nemen naar $dx$.
\begin{align}
 \int y^2\dfrac{dy}{dx} dx &= \int e^{x} dx
\end{align}

De integraal $\dfrac{dy}{dx}dx$ vereenvoudigen tot $dy$.
\begin{align}
 \int y^2 dy &= \int e^{x} dx
\end{align}

De primitieven nemen van beide kanten.
\begin{align}
 \frac{1}{3}y^3 + C_1 & = e^x + C_2\\
 \frac{1}{3}y^3  & = e^x + C_3\\
 y^3  & = 3e^x + C_4\\
 y  & = \sqrt[3]{3e^x + C} \qquad \text{met } C \in \mathbb{R}
\end{align}
```

## Opgaven 2.1c

```{admonition} Uitwerkingen
:class: dropdown

\begin{align*}
 \dfrac{dy}{dx} = y\sin(x)
\end{align*}

Alle variabelen met een $y$ naar links en variabelen met een $x$ naar rechts.
\begin{align}
 \dfrac{1}{y}\dfrac{dy}{dx} &= \sin(x)
\end{align}

Aan beide kanten de integraal nemen naar $dx$.
\begin{align}
 \int \dfrac{1}{y}\dfrac{dy}{dx} dx &= \int \sin(x) dx
\end{align}

De integraal $\dfrac{dy}{dx}dx$ vereenvoudigen tot $dy$.
\begin{align}
 \int \dfrac{1}{y} dy &= \int \sin(x) dx
\end{align}

De primitieven nemen van beide kanten.
\begin{align}
 \ln|y|  + C_1 &=  -\cos(x) + C_2\\
 \ln|y|  &=  -\cos(x) + C_3\\
 e^{\ln|y|}  &=  e^{-\cos(x) + C_3}\\
 |y|  &=  e^{-\cos(x) + C_3}\\
 |y|  &=  e^{-\cos(x)} \cdot e^{C_3}\\
 y  &=  \pm e^{-\cos(x)} \cdot e^{C_3}
\end{align}

$y = 0$ voldoet aan de dv, dus
\begin{align}
 y  &=  Ce^{-\cos(x)} \qquad \text{met } C \in \mathbb{R}
\end{align}
```

## Opgaven 2.1d

```{admonition} Uitwerkingen
:class: dropdown

\begin{align*}
 (x+3)\dfrac{dy}{dx} = 2(y+2)
\end{align*}

Alle variabelen met een $y$ naar links en variabelen met een $x$ naar rechts.
\begin{align}
 \frac{1}{(y+2)} \dfrac{dy}{dx} &= \dfrac{2}{(x+3)}
\end{align}

Aan beide kanten de integraal nemen naar $dx$.
\begin{align}
 \int \frac{1}{(y+2)} \dfrac{dy}{dx} dx &= \int \dfrac{2}{(x+3)}dx
\end{align}

De integraal $\dfrac{dy}{dx}dx$ vereenvoudigen tot $dy$.
\begin{align}
 \int \frac{1}{(y+2)} dy &= \int \dfrac{2}{(x+3)}dx
\end{align}

De primitieven nemen van beide kanten.
\begin{align}
 \ln|y+2| + C_1 &=  2\ln|x+3| + C_2\\
 \ln|y+2|  &=  2\ln|x+3| + C_3\\
 e^{\ln|y+2|} &=  e^{2\ln|x+3| + c_3}\\
 |y+2| &=  e^{2\ln|x+3| + c_3}\\
 |y+2| &=  e^{\ln(x+3)^2 + c_3}\\
 |y+2| &=  e^{\ln(x+3)^2} \cdot  e^{c_3}\\
 |y+2| &=  (x+3)^2 \cdot  e^{c3}\\
 y+2 &=  \pm (x+3)^2 \cdot  e^{c3}
\end{align}

$y+2 = 0$ voldoet aan de dv, dus
\begin{align}
 y+2 &=  C\cdot  (x+3)^2 &\qquad \text{met } C \in \mathbb{R} \\
 y &=  C\cdot  (x+3)^2 - 2 &\qquad \text{met } C \in \mathbb{R}
\end{align}
```

## Opgaven 2.2a

```{admonition} Uitwerkingen
:class: dropdown

\begin{align*}
 \sqrt{1-x^2}\dfrac{dy}{dx} = -y^2 \qquad y(0)=\frac{1}{2}
\end{align*}

Alle variabelen met een $y$ naar links en variabelen met een $x$ naar rechts.
\begin{align}
 -\dfrac{1}{y^2}\dfrac{dy}{dx} &= \dfrac{1}{\sqrt{1-x^2}}
\end{align}

Aan beide kanten de integraal nemen naar $dx$.
\begin{align}
 \int -\dfrac{1}{y^2}\dfrac{dy}{dx} dx &= \int \dfrac{1}{\sqrt{1-x^2}} dx
\end{align}

De integraal $\dfrac{dy}{dx}dx$ vereenvoudigen tot $dy$.
\begin{align}
 \int -\dfrac{1}{y^2} dy &= \int \dfrac{1}{\sqrt{1-x^2}} dx
\end{align}

De primitieven nemen van beide kanten.
\begin{align}
 \frac{1}{y} + C_1 &= \arcsin(x) + C_2\\
 \frac{1}{y} &= \arcsin(x) + C_3 \\
 y &= \frac{1}{\arcsin(x) + C} \qquad \text{met } C \in \mathbb{R}
\end{align}

De beginvoorwaarde gebruiken voor het vinden van de constante C.

Er geldt  $y(0)=\frac{1}{2}$ dus,

\begin{align}
 \frac{1}{2} &= \frac{1}{\arcsin(0) + C} \\
 \frac{1}{2} &= \frac{1}{0 + C} \\
 C &= 2
\end{align}

De constante invullen in de gevonden algemene oplossing geeft;
\begin{align}
 y &= \frac{1}{\arcsin(x) + 2}
\end{align}
```

## Opgaven 2.2b

```{admonition} Uitwerkingen
:class: dropdown

\begin{align*}
 -x\dfrac{dy}{dx} = \frac{1+y^2}{y}  \qquad y(1)=2
\end{align*}

Alle variabelen met een $y$ naar links en variabelen met een $x$ naar rechts.
\begin{align}
 \frac{y}{1+y^2} \dfrac{dy}{dx} &= -\frac{1}{x}
\end{align}

Aan beide kanten de integraal nemen naar $dx$.
\begin{align}
\int \frac{y}{1+y^2} \dfrac{dy}{dx} dx &= \int -\frac{1}{x} dx
\end{align}

De integraal $\dfrac{dy}{dx}dx$ vereenvoudigen tot $dy$
\begin{align}
 \int \frac{y}{1+y^2} dy &= \int -\frac{1}{x} dx
\end{align}

Gebruik de substitutie methode,
\begin{align}
 \text{stel: }  u &= 1+y^2 \\
 du &= 2y dy\\
 \frac{1}{2} du &= y dy
\end{align}

Vervang $y dy$ door $\frac{1}{2} du$
\begin{align}
 \int \frac{1}{2}\frac{1}{u} du &= \int -\frac{1}{x} dx \\
 \frac{1}{2}\ln|u|  + C_1 &= -\ln|x| + C_2 \\
 \frac{1}{2}\ln|u|  &= -\ln|x| + C_3 \\
 \ln|u|^{\frac{1}{2}} &= \ln|x|^{-1} + C_3 \\
 e^{\ln|u|^{\frac{1}{2}}} &= e^{\ln|x|^{-1} + C_3 }\\
 |u|^{\frac{1}{2}} &= e^{\ln|x|^{-1} + C_3 }\\
 |u|^{\frac{1}{2}} &= e^{\ln|x|^{-1}} \cdot e^{C_3} \\
 |u|^{\frac{1}{2}} &= |x|^{-1} \cdot e^{C_3} \\
 |u|^{\frac{1}{2}} &= \dfrac{1}{x}\cdot e^{C_3} \\
 |u| &= \dfrac{1}{x^2}\cdot e^{C_3} \\
 u &= \pm \dfrac{1}{x^2}\cdot e^{C_3}
\end{align}

De oorspronkelijke waarde invullen dus $u = 1+y^2$
\begin{align}
 1 + y^2 &= \dfrac{1}{x^2}\cdot e^{C_3} \\
 y^2 &=  \dfrac{1}{x^2}\cdot e^{C_3} -1\\
 y &= \pm \sqrt{\dfrac{1}{x^2}\cdot e^{C_3} -1}\\
 y &= \pm \sqrt{\dfrac{C}{x^2}  -1} \qquad \text{met } C \in \mathbb{R}
\end{align}

De beginvoorwaarde gebruiken voor het vinden van de constante C. \\Er geldt  $y(1)=2 $, dus
\begin{align}
 2 &= \pm \sqrt{\dfrac{C}{1^2}  -1}\\
 4 &= C  -1\\
 C &= 5
\end{align}

De constante invullen in de gevonden algemene oplossing geeft;
\begin{align}
 y &= \pm \sqrt{\dfrac{5}{x^2}  -1}
\end{align}


\setcounter{equation}{0}
```

## Opgaven 2.2c

```{admonition} Uitwerkingen
:class: dropdown

\begin{align*}
 \dfrac{dy}{dx} = \dfrac{2x}{1+y^2} \qquad y(2)=3
\end{align*}

Alle variabelen met een $y$ naar links en variabelen met een $x$ naar rechts.
\begin{align}
 {1+y^2} \dfrac{dy}{dx} &= 2x
\end{align}

Aan beide kanten de integraal nemen naar $dx$.
\begin{align}
 \int {1+y^2} \dfrac{dy}{dx} dx &= \int 2x dx
\end{align}

De integraal $\dfrac{dy}{dx}dx$ vereenvoudigen tot $dy$.
\begin{align}
 \int {1+y^2} dy &= \int 2x dx
\end{align}

De primitieven nemen van beide kanten.
\begin{align}
 y + \frac{1}{3}y^3 + C_1 &= x^2 + C_2 \\
 y + \frac{1}{3}y^3  &= x^2 + C \qquad \text{met } C \in \mathbb{R}
\end{align}

De beginvoorwaarde gebruiken voor het vinden van de constante C.

Er geldt $y(2)=3$ dus,

\begin{align}
 3 + \frac{1}{3}\cdot 3^3  &= 2^2 + C \\
 12  &= 4 + C \\
 C = 8
\end{align}

De constante invullen in de gevonden algemene oplossing geeft;
\begin{align}
 \frac{1}{3}y^3 + y &= x^2 + 8
\end{align}
```
