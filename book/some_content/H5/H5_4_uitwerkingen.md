# 5.4 Uitwerkingen

## Opgaven 5.1a

```{admonition} Uitwerkingen
:class: dropdown

  Voor een RC-kring geldt:
  \begin{align}
   U(t) &= U_r + U_c   \\
     &= R \cdot I + \dfrac{1}{C} \int I dt
  \end{align}
  
  Beide zijdes differenti\"eren geeft de gevraagde DV.:
  \begin{align}
   \dfrac{dU(t)}{dt} &= R \cdot \dfrac{dI}{dt} + \dfrac{1}{C} \cdot  I
  \end{align}


  De gegevens invullen in de DV geeft:
  \begin{align}
   \dfrac{dU(t)}{dt} &= 100 \cdot \dfrac{dI}{dt} + \dfrac{1}{0.1} \cdot  I\\
   0 &= 100 \cdot \dfrac{dI}{dt} + \dfrac{1}{0.1} \cdot  I \\
   0 &= 100 \cdot \dfrac{dI}{dt} + 10 \cdot  I
  \end{align}
  
%De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
%\begin{align*}
% I = I_h + I_p
%\end{align*}

De homogene D.V. wordt:
\begin{align}
 100\dfrac{dI}{dt} + 10I = 0
\end{align}

Als oplossing voor de homogene D.V. stel:
\begin{align}
 I = Ce^{\lambda t} \text{ met } C \in \mathbb{R}
\end{align}

Invullen in de D.V. geeft:
\begin{align}
 100\lambda \cdot Ce^{\lambda t} + 10\cdot Ce^{\lambda t} &= 0 \\
 (100\lambda +10 )\cdot Ce^{\lambda t}  &= 0
\end{align}

De vergelijking moet gelden voor alle waardes van C dus ook voor $C \neq 0$. \
Verder geldt dat $e^{\lambda t} \neq 0 $ dus,
\begin{align}
 100\lambda +10   &= 0  \\
 100\lambda   &= -10 \\
 \lambda   &= -\dfrac{1}{10}
\end{align}

De waarde voor $\lambda$ invullen in de homogene oplossing geeft;
\begin{align}
 I = Ce^{-\frac{1}{10}t} \qquad \text{met } C \in \mathbb{R}
\end{align}

De gegeven voorwaarden gebruiken om C te bepalen.  $I(0) = 1$

Dus invullen geeft:
\begin{align}
 1 &= Ce^{-\frac{1}{10} \cdot 0}  \\
 1 &= C \cdot 1
\end{align}

Hieruit volgt:
\begin{align}
 C &= 1
\end{align}

Dus C invullen in de totale oplossing geeft:
\begin{align}
 I &= 1 \cdot e^{-\frac{1}{10}t}
\end{align}
```

## Opgaven 5.1b

```{admonition} Uitwerkingen
:class: dropdown

  Voor een RC-kring geldt:
  \begin{align}
   U(t) &= U_r + U_c   \\
     &= R \cdot I + \dfrac{1}{C} \int I dt
  \end{align}
  
  Beide zijdes differenti\"eren geeft de gevraagde DV.:
  \begin{align}
   \dfrac{dU(t)}{dt} &= R \cdot \dfrac{dI}{dt} + \dfrac{1}{C} \cdot  I
  \end{align}

  
  De gegevens invullen in de DV geeft:
  \begin{align}
   \dfrac{dU(t)}{dt} &= 20 \cdot \dfrac{dI}{dt} + \dfrac{1}{0.2} \cdot  I\\
   -100 \sin(t) &= 20 \cdot \dfrac{dI}{dt} + \dfrac{1}{0.2} \cdot  I \\
   -100 \sin(t) &= 20 \cdot \dfrac{dI}{dt} + 5 \cdot  I
  \end{align}
  
De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
\begin{align*}
 I = I_h + I_p
\end{align*}

De homogene D.V. wordt:
\begin{align}
 20\dfrac{dI}{dt} + 5I = 0
\end{align}

Als oplossing voor de homogene D.V. stel:
\begin{align*}
 I_h = Ce^{\lambda t} \text{ met } C \in \mathbb{R}
\end{align*}

Invullen in de D.V. geeft:
\begin{align}
 20\lambda \cdot Ce^{\lambda t} + 5\cdot Ce^{\lambda t} &= 0 \\
 (20\lambda +5 )\cdot Ce^{\lambda t}  &= 0
\end{align}

De vergelijking moet gelden voor alle waardes van C dus ook voor $C \neq 0$. \
Verder geldt dat $e^{\lambda t} \neq 0 $ dus,
\begin{align}
 20\lambda +5   &= 0  \\
 20\lambda   &= -5 \\
 \lambda   &= -\dfrac{1}{4}
\end{align}

De waarde voor $\lambda $ invullen in de homogene oplossing geeft;
\begin{align}
 I_h = Ce^{-\frac{1}{4}t} \qquad \text{met } C \in \mathbb{R}
\end{align}

Kies als vorm voor de particuliere oplossing een vorm die gelijk is aan het rechterlid van de D.V.  
Als vorm voor de particuliere oplossing stel:
\begin{align}
 I_p &=  C_1\cos(t) + C_2\sin(t) \\
 I'_p &= -C_1\sin(t) + C_2\cos(t)
\end{align}

Invullen in de D.V. geeft:
\begin{align}
 20 \cdot (-C_1\sin(t) + C_2\cos(t)) +  5 (C_1 \cos(t)+C_2 \sin(t)) &=  -100\sin(t) \\
 (5C_1+20C_2)\cos(t) + (-20C_1+5C_2)\sin(t) &= -100\sin(t)
\end{align}

De co\"effici\"enten moeten links en rechts gelijk zijn dus volgt:
\begin{align}
 5C_1+20C_2 &= 0 \\
 -20C_1+5C_2 &= -100
\end{align}


Hieruit volgt:
\begin{align}
 5C_1 &= -20C_2 \\
 C_1 &= -4C_2
\end{align}

$C_1 $ invullen geeft:
\begin{align}
 -20 \cdot (-4C_2) + 5 \cdot (C_2) &= -100\\
 85C_1  &= -100\\
  C_2 &= -\dfrac{100}{85} = -\dfrac{20}{17}
\end{align}


$C_2 $ invullen geeft:
\begin{align}
 C_1 &= -4C_2  \\
 C_1 &= -4 \cdot -\dfrac{20}{17}  \\
 C_1 &= \dfrac{80}{17}
\end{align}

De waardes voor $C_1$, $C_2$  invullen in de particuliere oplossing geeft:
\begin{align}
 I_p = \dfrac{80}{17}\cos(t) - \dfrac{20}{17}\sin(t)
\end{align}

De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
\begin{align}
 I &= I_h + I_p \\
 I &= Ce^{-\frac{1}{4}t}  +\dfrac{80}{17}\cos(t) - \dfrac{20}{17}\sin(t)\qquad \text{met } C \in \mathbb{R}  
\end{align}

De gegeven voorwaarden gebruiken om C te bepalen.  $I(0) = 2$

Dus invullen geeft:
\begin{align}
 2 &= Ce^{- \cdot 0} +\dfrac{80}{17}\cos(0) - \dfrac{20}{17}\sin(0)  \\
 2 &= C \cdot 1 +\dfrac{80}{17}\cdot 1 - \dfrac{20}{17}\cdot 0
\end{align}

Hieruit volgt:
\begin{align}
 C &= 2 - \dfrac{80}{17} \\
 C &= - \dfrac{46}{17}
\end{align}

Dus C invullen in de totale oplossing geeft:
\begin{align}
 I &= - \dfrac{46}{17} e^{-\frac{1}{4}t}  +\dfrac{80}{17}\cos(t) - \dfrac{20}{17}\sin(t)
\end{align}
```

## Opgaven 5.2a

## Opgaven 5.2b

## Opgaven 5.3a

```{admonition} Uitwerkingen
:class: dropdown

  Voor een RL-kring geldt:
  \begin{align}
   U(t) &= U_r + U_s   \\
     &= R \cdot I + L \cdot \dfrac{dI}{dt}
  \end{align}

  %Beide zijdes differenti\"eren geeft de gevraagde DV.:
  %\begin{align*}
  % \dfrac{dU(t)}{dt} &= R \cdot \dfrac{dI}{dt} + \dfrac{1}{C} \cdot  I
  %\end{align*}

  De gegevens invullen in de DV geeft:
  \begin{align}
   U(t) &=  \dfrac{1}{2} \cdot \dfrac{dI}{dt}  + 10 \cdot I \\
   50 \sin(t) &= \dfrac{1}{2} \cdot \dfrac{dI}{dt} + 10 \cdot  I
  \end{align}
```

## Opgaven 5.3b

```{admonition} Uitwerkingen
:class: dropdown

De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
\begin{align}
 I = I_h + I_p
\end{align}

De homogene D.V. wordt:
\begin{align}
 \dfrac{1}{2} \dfrac{dI}{dt} + 10I = 0
\end{align}

Als oplossing voor de homogene D.V. stel:
\begin{align}
 I_h = Ce^{\lambda t} \text{ met } C \in \mathbb{R}
\end{align}

Invullen in de D.V. geeft:
\begin{align}
 \dfrac{1}{2} \lambda \cdot Ce^{\lambda t} + 10\cdot Ce^{\lambda t} &= 0 \\
 (\dfrac{1}{2}\lambda +10 )\cdot Ce^{\lambda t}  &= 0
\end{align}

De vergelijking moet gelden voor alle waardes van C dus ook voor $C \neq 0$. \
Verder geldt dat $e^{\lambda t} \neq 0 $ dus,
\begin{align}
 \dfrac{1}{2}\lambda +10   &= 0  \\
 \dfrac{1}{2} \lambda   &= -10 \\
 \lambda   &= -20
\end{align}

De waarde voor $\lambda $ invullen in de homogene oplossing geeft;
\begin{align}
 I_h = Ce^{-20t} \qquad \text{met } C \in \mathbb{R}
\end{align}

Kies als vorm voor de particuliere oplossing een vorm die gelijk is aan het rechterlid van de D.V.
Als vorm voor de particuliere oplossing stel:
\begin{align}
 I_p &=  C_1\cos(t) + C_2\sin(t) \\
 I'_p &= -C_1\sin(t) + C_2\cos(t)
\end{align}

Invullen in de D.V. geeft:
\begin{align}
 \dfrac{1}{2} \cdot (-C_1\sin(t) + C_2\cos(t)) +  10 (C_1 \cos(t)+C_2 \sin(t)) &=  50\sin(t) \\
 (10C_1+\dfrac{1}{2}C_2)\cos(t) + (-\dfrac{1}{2}C_1+10C_2)\sin(t) &= 50\sin(t)
\end{align}

De co\"effici\"enten moeten links en rechts gelijk zijn dus volgt:
\begin{align}
 10C_1+\dfrac{1}{2}C_2 &= 0 \\
 -\dfrac{1}{2}C_1+10C_2 &= 50
\end{align}

Hieruit volgt:
\begin{align}
 \dfrac{1}{2}C_2 &= -10C_1 \\
 C_2 &= -20C_1
\end{align}

$C_2 $ invullen geeft:
\begin{align}
 -\dfrac{1}{2}C_1+10 \cdot (-20C_1) &= 50\\
 -200\dfrac{1}{2}C_1  &= 50\\
  C_1 &= -\dfrac{100}{401}  
\end{align}

$C_1 $ invullen geeft:
\begin{align}
 C_2 &= -20C_1  \\
 C_2 &= -20 \cdot -\dfrac{100}{401}   \\
 C_2 &= \dfrac{2000}{401}
\end{align}

De waardes voor $C_1$, $C_2$  invullen in de particuliere oplossing geeft:
\begin{align}
 I_p = -\dfrac{100}{401}\cos(t) + \dfrac{2000}{401}\sin(t)
\end{align}

De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
\begin{align}
 I &= I_h + I_p \\
 I &= Ce^{-20t}  -\dfrac{100}{401}\cos(t) + \dfrac{2000}{401}\sin(t) \qquad \text{met } C \in \mathbb{R}  
\end{align}

De gegeven voorwaarden gebruiken om C te bepalen.  $I(0) = 0$

Dus invullen geeft:
\begin{align}
 0 &= Ce^{-20 \cdot 0}  -\dfrac{100}{401}\cos(0) + \dfrac{2000}{401}\sin(0)  \\
 0 &= C \cdot 1 -\dfrac{100}{401} \cdot 1 + \dfrac{2000}{401} \cdot 0
\end{align}

Hieruit volgt:
\begin{align}
 C &= \dfrac{100}{401}
\end{align}

Dus C invullen in de totale oplossing geeft:
\begin{align}
 I &= \dfrac{100}{401} e^{-20t}  -\dfrac{100}{401}\cos(t) + \dfrac{2000}{401}\sin(t)
\end{align}
```

## Opgaven 5.4a

```{admonition} Uitwerkingen
:class: dropdown

  Voor een losgelaten kogel geldt:
  \begin{align}
   F_{res} &= F_z - F_w   \\
   F_{res} &= m \cdot g -  k \cdot V \\
   m \cdot a &= m \cdot g -  k \cdot V \\
   a &= \dfrac{m}{m} \cdot g -  \dfrac{k}{m} \cdot V \\
   a &=  g -  \dfrac{k}{m} \cdot V
  \end{align}
  
  Schrijf de versnelling $a$ als afgeleide van de snelheid $v$ en herschrijf:
  \begin{align}
   \dfrac{dV}{dt} &=  g -  \dfrac{k}{m} \cdot V \\
   \dfrac{dV}{dt} + \dfrac{k}{m} \cdot V &= g
  \end{align}
  

  %Beide zijdes differenti\"eren geeft de gevraagde DV.:
  %\begin{align*}
  % \dfrac{dU(t)}{dt} &= R \cdot \dfrac{dI}{dt} + \dfrac{1}{C} \cdot  I
  %\end{align*}

  
  De gegevens invullen in de DV geeft:
  \begin{align}
   \dfrac{dV}{dt} + \dfrac{0.1}{0.2} \cdot V &= 9.81  \\
   \dfrac{dV}{dt} + \dfrac{1}{2} \cdot V &= 9.81
  \end{align}
```

## Opgaven 5.4b

```{admonition} Uitwerkingen
:class: dropdown

De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
\begin{align}
 V = V_h + V_p
\end{align}

De homogene D.V. wordt:
\begin{align}
 \dfrac{dV}{dt} + \dfrac{1}{2} \cdot V &= 0
\end{align}

Als oplossing voor de homogene D.V. stel:
\begin{align}
 V_h = Ce^{\lambda t} \text{ met } C \in \mathbb{R}
\end{align}

Invullen in de D.V. geeft:
\begin{align}
  \lambda \cdot Ce^{\lambda t} + \dfrac{1}{2} \cdot Ce^{\lambda t} &= 0 \\
 (\lambda +\dfrac{1}{2} )\cdot Ce^{\lambda t}  &= 0
\end{align}

De vergelijking moet gelden voor alle waardes van C dus ook voor $C \neq 0$. \
Verder geldt dat $e^{\lambda t} \neq 0 $ dus,
\begin{align}
 \lambda + \dfrac{1}{2}   &= 0  \\
 \lambda   &= -\dfrac{1}{2}
\end{align}

De waarde voor $\lambda $ invullen in de homogene oplossing geeft;
\begin{align}
 V_h = Ce^{-\frac{1}{2}t} \qquad \text{met } C \in \mathbb{R}
\end{align}

Kies als vorm voor de particuliere oplossing een vorm die gelijk is aan het rechterlid van de D.V.  
Als vorm voor de particuliere oplossing stel:
\begin{align}
 V_p &=  C_1 \\
 V'_p &= 0
\end{align}

Invullen in de D.V. geeft:
\begin{align}
 0 + \dfrac{1}{2} \cdot C_1 &= 9.81\\
\end{align}

Hieruit volgt:
\begin{align}
 \dfrac{1}{2} \cdot C_1 &= 9.81 \\
 C_1 &= \dfrac{9.81}{\dfrac{1}{2}} = 19.62
\end{align}

De waardes voor $C_1$ invullen in de particuliere oplossing geeft:
\begin{align}
 V_p = 19.62
\end{align}

De algemene oplossing bestaat uit een optelling van de homogene oplossing en de particuliere oplossing.
\begin{align}
 V &= V_h + V_p \\
 V &=  Ce^{-\frac{1}{2}t} + 19.62 \qquad \text{met } C \in \mathbb{R}  
\end{align}

De gegeven voorwaarden gebruiken om C te bepalen.  $V(0) = 0$

Dus invullen geeft:
\begin{align}
 0 &= Ce^{-\frac{1}{2} \cdot 0} + 19.62  \\
 0 &= C \cdot 1 + 19.62 \cdot 0
\end{align}

Hieruit volgt:
\begin{align}
 C &= -19.62
\end{align}

Dus C invullen in de totale oplossing geeft:
\begin{align}
 V &= -19.62e^{-\frac{1}{2}t} + 19.62
\end{align}

De eindsnelheid van de kogel is:\
als $t$ naar $\infty$ nadert dan gaat $V$ naar 19.62 m/s
```