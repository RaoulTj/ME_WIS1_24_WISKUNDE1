# 6.4 Uitwerkingen

## Opgaven 6.1a

```{admonition} Uitwerkingen
:class: dropdown

  Voor een RLC-kring geldt:
  \begin{align}
   U(t) &= U_L + U_r +  U_c    \\
     &=  L \cdot \dfrac{dI}{dt} + R \cdot I +\dfrac{1}{C} \int I dt
  \end{align}

  Beide zijdes differenti\"eren geeft de gevraagde DV.:
  \begin{align}
   \dfrac{dU(t)}{dt} &= L \cdot \dfrac{d^2I}{dt^2} + R \cdot \dfrac{dI}{dt} + \dfrac{1}{C} \cdot  I
  \end{align}

  De gegevens invullen in de DV geeft:
  \begin{align}
   \dfrac{dU(t)}{dt} &= 1 \cdot \dfrac{d^2I}{dt^2} + 20 \cdot \dfrac{dI}{dt} + \dfrac{1}{0.1} \cdot  I\\
   0 &= 1 \cdot \dfrac{d^2I}{dt^2} + 20 \cdot \dfrac{dI}{dt} + \dfrac{1}{0.1} \cdot  I\\
   0 &= \dfrac{d^2I}{dt^2} + 20 \cdot \dfrac{dI}{dt} + 10 \cdot  I
  \end{align}

%De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
%\begin{align*}
% I = I_h + I_p
%\end{align*}

De homogene D.V. wordt:
\begin{align}
 \dfrac{d^2I}{dt^2} + 20\dfrac{dI}{dt} + 10I = 0
\end{align}

Als oplossing voor de homogene D.V. stel:
\begin{align}
 I = Ce^{\lambda t} \text{ met } C \in \mathbb{R}
\end{align}

Invullen in de D.V. geeft:
\begin{align}
 \lambda^2 \cdot Ce^{\lambda t} +100\lambda \cdot Ce^{\lambda t} + 10\cdot Ce^{\lambda t} &= 0 \\
 (\lambda^2 + 20\lambda +10 )\cdot Ce^{\lambda t}  &= 0
\end{align}

De vergelijking moet gelden voor alle waardes van C dus ook voor $C \neq 0$. \
Verder geldt dat $e^{\lambda t} \neq 0 $ dus,
\begin{align}
 \lambda^2 + 20\lambda +10   &= 0
\end{align}

Dus de discriminant is,
\begin{align}
 D = (20)^2 - 4 \cdot 1 \cdot 10 = 400-40=360
\end{align}

De oplossingen van de karakteristieke vergelijking zijn:
\begin{align}
  \lambda_{1,2} &= \dfrac{-20 \pm \sqrt{360}}{2 \cdot 1}\\
  \lambda_{1,2} &= \dfrac{-20 \pm 6\sqrt{10}}{2 \cdot 1}\\
  \lambda_{1} &= -10 + 3\sqrt{10} =  -0.51\\
 \lambda_{2} &= -10 - 3\sqrt{10} = -19.49\\
\end{align}

De waarde voor $\lambda$ invullen in de algemene oplossing geeft;
\begin{align*}
 I_h = C_1e^{\lambda_1 x} + C_2e^{\lambda_1 x} \qquad \text{met } C \in \mathbb{R}
\end{align*}
\begin{align}
 I_h = C_1e^{-0.51x} + C_2e^{-19.49x} \qquad \text{met } C \in \mathbb{R}
\end{align}

De gegeven voorwaarden gebruiken om $C_1$ en $C_2$ te bepalen.  $I(0) = 0$ en $I'(0) = 1$

Dus invullen geeft voor $I(0) = 0$:
\begin{align}
 0 &= C_1e^{-0.51 \cdot 0} + C_2e^{-19.49 \cdot 0} \\
 0 &= C_1e^{0} + C_2e^{0} \\
 0 &= C_1 \cdot 1 + C_2 \cdot 1 \\
 0 &= C_1 + C_2
\end{align}

Hieruit volgt:
\begin{align}
 C_1 &= -C_2
\end{align}

Dus invullen geeft voor $I'(0) = 1$:
\begin{align}
 1 &= -0.51C_1e^{-0.51 \cdot 0}  -19.49C_2e^{-19.49 \cdot 0} \\
 1 &= -0.51C_1e^{0}  -19.49C_2e^{0} \\
 1 &= -0.51C_1 \cdot 1  -19.49C_2 \cdot 1 \\
 1 &= -0.51C_1  -19.49C_2
\end{align}

$C_1$ invullen geeft:
\begin{align}
 1 &= -0.51 (-C_2)  -19.49C_2 \\
 1 &= 0.51C_2  -19.49C_2 \\
 1 &= -18.98C_2 \\
 C_2 &= -\dfrac{1}{18.98} = -0.0527
\end{align}

$C_2$ invullen geeft:
\begin{align}
 C_1 &= -C_2 = 0.0527
\end{align}

Dus $C_1$ en $C_2$ invullen in de  oplossing geeft:
\begin{align}
 I_h &=  0.0527e^{-0.51x} -0.0527e^{-19.49x}
\end{align}
```

## Opgaven 6.1b

```{admonition} Uitwerkingen
:class: dropdown

Voor een RLC-kring geldt:
  \begin{align}
   U(t) &= U_L + U_r +  U_c    \\
     &=  L \cdot \dfrac{dI}{dt} + R \cdot I +\dfrac{1}{C} \int I dt
  \end{align}

  Beide zijdes differenti\"eren geeft de gevraagde DV.:
  \begin{align}
   \dfrac{dU(t)}{dt} &= L \cdot \dfrac{d^2I}{dt^2} + R \cdot \dfrac{dI}{dt} + \dfrac{1}{C} \cdot  I
  \end{align}

  De gegevens invullen in de DV geeft:
  \begin{align}
   \dfrac{dU(t)}{dt} &= 5 \cdot \dfrac{d^2I}{dt^2} + 50 \cdot \dfrac{dI}{dt} + \dfrac{1}{2} \cdot  I\\
   -24\sin(t) &= 5 \cdot \dfrac{d^2I}{dt^2} + 50 \cdot \dfrac{dI}{dt} + \dfrac{1}{2} \cdot  I\\
   -24\sin(t) &=5 \cdot  \dfrac{d^2I}{dt^2} + 50 \cdot \dfrac{dI}{dt} + \dfrac{1}{2} \cdot  I
  \end{align}

%De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
%\begin{align*}
% I = I_h + I_p
%\end{align*}

De homogene D.V. wordt:
\begin{align}
 5\dfrac{d^2I}{dt^2} + 50\dfrac{dI}{dt} + \dfrac{1}{2}I = 0
\end{align}

Als oplossing voor de homogene D.V. stel:
\begin{align}
 I = Ce^{\lambda t} \text{ met } C \in \mathbb{R}
\end{align}

Invullen in de D.V. geeft:
\begin{align}
 5\lambda^2 \cdot Ce^{\lambda t} +50\lambda \cdot Ce^{\lambda t} + \dfrac{1}{2} \cdot Ce^{\lambda t} &= 0 \\
 (5\lambda^2 + 50\lambda +\dfrac{1}{2} )\cdot Ce^{\lambda t}  &= 0
\end{align}

De vergelijking moet gelden voor alle waardes van C dus ook voor $C \neq 0$. \
Verder geldt dat $e^{\lambda t} \neq 0 $ dus,
\begin{align}
 5\lambda^2 + 50\lambda +\dfrac{1}{2}   &= 0 \\
 10\lambda^2 + 100\lambda +1   &= 0
\end{align}

Dus de discriminant is,
\begin{align}
 D = (100)^2 - 4 \cdot 10 \cdot 1 = 10000-40=9960
\end{align}

De oplossingen van de karakteristieke vergelijking zijn:
\begin{align}
  \lambda_{1,2} &= \dfrac{-100 \pm \sqrt{9960}}{2 \cdot 10}\\
  \lambda_{1} &= -9.989\\
 \lambda_{2} &=  -0.010
\end{align}

De waarde voor $\lambda$ invullen in de algemene oplossing geeft;
\begin{align*}
 I_h = C_1e^{\lambda_1 x} + C_2e^{\lambda_1 x} \qquad \text{met } C \in \mathbb{R}
\end{align*}
\begin{align}
 I_h = C_1e^{-0.010x} + C_2e^{-9.989x} \qquad \text{met } C \in \mathbb{R}
\end{align}

Kies als vorm voor de particuliere oplossing een vorm die gelijk is aan het rechterlid van de D.V.
Als vorm voor de particuliere oplossing stel:
\begin{align}
 y_p =  C_1\sin(x) + C_2\cos(x)
\end{align}

Invullen in de D.V. geeft:
\begin{align}
 10 \cdot(-C_1\sin(x) - C_2\cos(x)) + 100 \cdot (C_1\cos(x) - C_2\sin(x)) + 1 \cdot (C_1\sin(x) + C_2\cos(x)) &= -48\sin(x) \\
 -10C_1\sin(x) - 10C_2\cos(x)  + 100C_1\cos(x) - 100C_2\sin(x)) +  C_1\sin(x) + C_2\cos(x)  = -48\sin(x) \\
 (-10C_1 + C_1 - 100C_2) \sin(x) + (100C_1+C_2-10C_2)\cos(x)   = -48\sin(x) \\
  (-9C_1 - 100C_2) \sin(x) + (100C_1-9C_2)\cos(x)   = -48\sin(x)
\end{align}

De co\"effici\"enten moeten links en rechts gelijk zijn dus volgt:
\begin{align}
 -9C_1 - 100C_2 &= -48 \\
 100C_1-9C_2 &= 0
\end{align}

Hieruit volgt:
\begin{align}
100C_1-9C_2 &= 0 \\
100C_1 &= 9C_2 \\
 C_1 &= 0.09C_2
\end{align}

$C_1 $ invullen geeft:
\begin{align}
 -9 \cdot 0.09C_2 - 100C_2 &= -48\\
  0.81C_2 + 100 C_2 &= -48\\
  100.81C_2 &= -48\\
  C_2 &= 0.476
\end{align}

$C_2 $ invullen geeft:
\begin{align}
 C_1 &= 0.09C_2 \\
 C_1 &= 0.09 \cdot 0.476\\
 C_1 &= 0.0429
\end{align}

De waardes voor $C_1$, $C_2$  invullen in de particuliere oplossing geeft:
\begin{align}
  I_p = 0.0429\sin(x) + 0.476\cos(x)
\end{align}

De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
\begin{align}
 I &= I_h + I_p \\
 I &= C_1e^{-0.010x} + C_2e^{-9.989x} + 0.0429\sin(x) + 0.476\cos(x)   \qquad \text{met } C \in \mathbb{R}
\end{align}

De gegeven voorwaarden gebruiken om $C_1$ en $C_2$ te bepalen.  $I(0) = 0$ en $I'(0) = 1$

Dus invullen geeft voor $I(0) = 0.5$:
\begin{align}
 0.5 &= C_1e^{-0.010 \cdot 0} + C_2e^{-9.989 \cdot 0} + 0.0429\sin(0) + 0.476\cos(0)  \\
 0.5 &= C_1e^{0} + C_2e^{0} + 0 + 0.476\\
 0.5 &= C_1  + C_2  + 0.476 \\
 0.024 &= C_1 + C_2
\end{align}

Hieruit volgt:
\begin{align}
 C_1 &= 0.024 -C_2
\end{align}

Dus invullen geeft voor $I'(0) = 1$:
\begin{align}
 1 &= -0.010C_1e^{-0.010 \cdot 0}  -9.989C_2e^{-9.989 \cdot 0} + 0.0429\cos(0) - 0.476\sin(0) \\
 1 &= -0.010C_1e^{0}  -9.989C_2e^{0} + 0.0429 - 0  \\
 1 &= -0.010C_1  -9.989C_2 + 0.0429  \\
 0.9571 &= -0.010C_1  -9.989C_2
\end{align}

$C_1$ invullen geeft:
\begin{align}
 0.9571 &= -0.010(0.024-C_2)  -9.989C_2  \\
 0.9571 &= 2.4\cdot 10^{-4} + 0.010C_2  -9.989C_2 \\
 0.95676 &= -9.979C_2\\
 C_2 &=  -0.0959
\end{align}

$C_2$ invullen geeft:
\begin{align}
 C_1 &= 0.024 - -0.0959\\
 C_1 &= 0.1199
\end{align}

Dus $C_1$ en $C_2$ invullen in de totale oplossing geeft:
\begin{align}
 I &= 0.1199e^{-0.010x} -0.0959e^{-9.989x} + 0.0429\sin(x) + 0.476\cos(x)
\end{align}
```