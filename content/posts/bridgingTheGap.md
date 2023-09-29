---
title: "Review Material for a First Electronics Course"
date: 2023-09-23T12:02:06-05:00
draft: false
---

<div style="background-color: #fcedbd; width:100%; padding: 20px;margin-left: auto; margin-right: auto; margin-botton: 25px;font-style: italic;border-radius:7px;"> 
After enrolling in electronics courses, many students are still connecting dots and developing fluency regarding prereq STEM concepts. Below is an article that addresses common questions, strategies and conceptual connections that I hope will aid students in their study of electronics. The takeaway is to practice, ask questions, then practice some more. Don't get discouraged. In my experience, it always feels like I have to re-learn the most important topics many times. -Dr. Beal
</div>

<br>

# <center> !!!UNDER CONSTRUCTION!!! </center>

<br>

### <center> Bridging the Gap between Circuits and Electronics </center>

<center>Aubrey N. Beal, Ph.D.  </center>
<center>Department of Electrical and Computer Engineering  </center>  
<center>The University of Alabama in Huntsville (UAH)  </center>

<h2></h2>

HOW do you get to Carnegie Hall? Practice. Irwin and Nelms propose that learning circuit analysis is similar to learning a musical instrument. [^fn1] During my undergraduate studies, a professor told me candidly that without hundreds of attempts at solving circuit problems many students may never obtain a passing grade. Practice. The same way that 'noodling' on a guitar doesn't often equip someone to play Purple Rain's solo, unstructured or under-practiced circuit study may seldom result in fluency of the tools used to build sophisticated electronic systems. This is true for electrical engineers, computer engineers, mechancial engineers, aerospace engineers, physicists, mathematicians, artists, CEOs, hobbyists, professors - *everybody*. The tutorial-based practice outlined below builds circuit analysis fundamentals and reinforces several specific skills that must be combined to analyze or design refined electonic systems. Where possible, examples (and associated references) are given such that the difficulty related to a particular set of exercises progressively escalates. If at any point an example feels overwhelming, you may want to rewind your study to a specific 'parachute point' that will be outlined at the begining of each section. The organization of this tutorial consists of the following sections:

<ol style = "list-style-type:upper-roman;margin-left:100px;">
  <li><a href="/posts/bridgingthegap/#i-differences-between-a-circuits-course-and-an-electronics-course">Differences between a 'circuits course' and an 'electronics course' </a></li>
  <li><a href=""><a href="/posts/bridgingthegap/#ii-basic-engineering-mathematics">Basic engineering mathematics</a> </li>
  <li><a href="/posts/bridgingthegap/#iii-ohms-law-and-i-v-curves">Ohm's law and I-V curves </a></li>
  <li><a href="/posts/bridgingthegap/#iv-kirchhoffs-voltage-law-kvl-and-circuit-loops">Kirchhoff's voltage law (KVL) and circuit 'loops' </a></li>
  <li><a href="/posts/bridgingthegap/#v-kirchhoffs-current-law-kcl-and-circuit-nodes">Kirchhoff's current law (KCL) and circuit 'nodes'  </a></li>
  <li><a href="/posts/bridgingthegap/#vi-mesh-analysis">Mesh analysis  </a></li>
  <li><a href="/posts/bridgingthegap/#vii-nodal-analysis">Nodal analysis </a></li>
  <li><a href="/posts/bridgingthegap/#viii-voltage-dividers-and-current-dividers">Voltage dividers and current dividers </a></li>
  <li><a href="/posts/bridgingthegap/#ix-series-and-parallel-elements">Series and parallel elements </a></li>
  <li><a href="/posts/bridgingthegap/#x-th%C3%A9venin--norton-equivalent-circuits">Thévenin & Norton equivalent circuits </a></li>
    <li><a href="/posts/bridgingthegap/#xi-energy-storage-elements">Energy storage elements </a></li>
  <li><a href="/posts/bridgingthegap/#xii-time-domain-solutions-for-transient-rc-circuits">Time-domain solutions for transient RC circuits </a></li>
  <li><a href="/posts/bridgingthegap/#xiii-laplace-transforms-notions-for-frequency-domain-rc-circuits">Laplace transforms (notions for frequency-domain RC circuits) </a></li>
  <li><a href="/posts/bridgingthegap/#xiv-complex-numbers-rational-polynomials-sinusoids-magnitude--phase">Complex numbers, rational polynomials, sinusoids, magnitude & phase</a></li>
  <li><a href="/posts/bridgingthegap/#xv-log-functions-decibels-and-their-plots">Log functions, decibels and their plots </a></li>
    <li><a href="/posts/bridgingthegap/#xvi-simple-rc-filters">Simple RC filters</a></li>
</ol>
 

### I. Differences between a 'circuits course' and an 'electronics course'
Circuits courses provide foundational concepts and tools needed to analyze and design sophisticated hardware related to electrical, electronic, power, computer, and electro-mechanical systems. A circuits course builds on basic physics, linear algebra and differential equations to analze various electrical component configurations as abstractions electrical/electronic systems. Electronics courses provide useful configurations and physical models with the aim of processing signals. An electronics course uses results and patterns from a circuits course (and other prereqs). Electronics as a discipline aims to create systems the reliably perform a function (usually with inputs and outputs). Electronics courses involve more complex devices and mathematics which are enabled by semiconductor-based solid-state-physics models and engineering-oriented applied math techniques involving input-output relationships.
 
 > *A circuits course is similar to a collection of Sodoku puzzles. The puzzles are fun and require skills, practice and problem-solving. However, the completed puzzles not valuable beyond entertainment or achieving proficiency towards the underlying problem solving mechanisms.*

Both circuits and electronics courses aim to identify, model and predict the behavior of electrical/electronic circuits. Below is a table of some of the finer points that often differ between the two courses:

| 		| Circuits Course 		| Electronics Course	 	|
|--- 		| --- 				| --- 				|
|**Goals:**	| Introduce concepts		| Apply concepts		|
|		| Build problem solving skills	| Process and store signals	|
|**Texts:**	|Nilsson, James William, and Susan A. Riedel. Electric circuits. Pearson Education Limited, 2020.   |Sedra, A., Smith, K. C., Carusone, T. C., & Gaudet, V. (2020). Microelectronic circuits 8th edition.			|
|		|Irwin, J. D., & Nelms, R. M. (2020). Basic engineering circuit analysis (12th ed.). John Wiley & Sons.   |Jaeger, R. C., Blalock, T. N., & Blalock, B. J. (1997). Microelectronic circuit design (pp. 1033-1036). New York: McGraw-Hill.			|
|		|Hayt, W. H. (2024). Engineering Circuit Analysis (10th ed.), McGraw-Hill Education |Razavi, B. (2021). Fundamentals of microelectronics. John Wiley & Sons.			|
|**Concepts:**	|Elementary components 		|Complex & active components		|
|		|Resistor, capacitors, inductors|Diodes, transistors, amplifiers		|
|		|I-V curves			|Input/output relationships		|
|		|Linear (Ohmic) relationships	|Linear & nonlinear relationships	|
|		|Systems of equations		|Iterative/simulation solutions		|
|		|Exact solutions		|Approximations				|
|		|Basic physics models		|Solid-state physics models		|

### II. Basic engineering mathematics
These courses use mathematics. At a minimal, first glance, students should be comfortable with concepts like fractions, algegbra, trigonometry, solving systems of equations, exponential functions, logarithmic functions, complex numbers, rational functions, complex exponential-sinusoidal function relationship. As a parachute point consider a pre-calculus textbook [^fn2]. Alternatively, some signals & systems textbooks provide comprehensive reviews of basic engineering mathematics that are needed [^fn3].
 
### III. Ohm's law and I-V curves 

$$ I_T = G V_T = \frac{V_T}{R}$$

![Intro to basic I-V curves](/btg_IntroIVCurves.svg)
*<center>Details for Ohmic I-V characteristic curves measured by applying a test votage, measuring a test current and plotting the resulting relationship implied via Ohm's law.</center>*

![Examples of I-V curves](/btg_ResistiveIVCurves.svg)
*<center>Various I-V curve examples</center>*

### IV. Kirchhoff's voltage law (KVL) and circuit 'loops' 
### V. Kirchhoff's current law (KCL) and circuit 'nodes'
### VI. Mesh analysis

**Level 1 Mesh Analysis:** Consider the following circuit:
![Level 1 mesh circuit](/btg_meshLevel1.svg)
*<center>Level 1 mesh analysis circuit example</center>*
This circuit has two meshes and leads to an analysis with two equations and two unknowns. The $20m\text{A}$ current source $I_S$ gives a constraint equation. First, we define the current in the left mesh to be $I_1$ and the current in the right mesh to be $I_2$ with the directions indicated in the figure. 
The constraint equation gives:
$$I_1-I_2 = -20m\text{A}.$$
This fast analysis comes at a cost. The $20m\text{A}$ current source may not be used again in our analysis, and it is common to both the left and right meshes. A supermesh along the outside elements (as illustrated in the figure) avoids the $20m\text{A}$ current source and gives the remaining, linearly independent equation needed. This outer, supermesh KVL equation gives:
$$-5V + I_1R_1 + I_2R3 + I_2R4 = 0V.$$

These equations are linear and may be scaled. If the resistors are scaled by 1/1000 and the currents are scaled by 1000, resulting system of equations becomes 
$$\begin{align}
I_1 - I_2 = -20A \newline 
2I_1 + 4I_2 = 5V \newline
\end{align}
$$

**Level 2 Mesh Analysis:** Consider the following circuit:
![Level 2 mesh circuit](/btg_meshLevel2a.svg)
*<center>Level 2 mesh analysis circuit example</center>*
This circuit has three meshes and leads to an analysis with three equations and three unknowns. Note that the $20m\text{A}$ current source $I_S$ gives a constraint equation. First, we define the current in the left mesh to be $I_1$ and the current in the right mesh to be $I_2$ with the directions indicated in the figure. The constraint equation gives:
$$I_2-I_3 = -20m\text{A}.$$

Note that two supermesh selections are possible to avoid $I_S$. Proceeding with the supermesh comprised by outermost loop gives the KVL equation:

$$-V_{S1}+V_{R1}+V_{R2}+V_{R3}+V_{R4}=0$$
$$-V_{S1}+I_1R_1+I_2R_2+I_3R_3+I_3R_4=0$$
$$2000I_1+500I_2+1000I_3+3000I_3=5V$$
$$2000I_1+500I_2+4000I_3=5V$$

The remaining equation may be obtained either by using the remaining supermesh or the left-most mesh. The left-most mesh gives the KVL equation:

$$-V_{S1}+I_1R_1+(I_1-I_2)R_5+V_{S2}=0$$
$$2000I_1+200I_1-200I_2=2V$$
$$2200I_1-200I_2=2V$$

These equations are linear and may be scaled. If the resistors are scaled by 1/1000 and the currents are scaled by 1000, resulting system of equations that can be written as the following matrix

$$
\begin{bmatrix}
0 & 1 & -1 \newline
2 & 0.5 & 4 \newline
2.2 & -0.2 & 0 
\end{bmatrix}
\begin{bmatrix}
I_1 \newline
I_2 \newline
I_3
\end{bmatrix}  =
\begin{bmatrix}
-20 \newline
5 \newline
2
\end{bmatrix} 
$$

This gives the solution $I_1=-0.583\mu A$, $I_2=-16.408mA$, and $I_3=3.592mA$.

**Level 3 Mesh Analysis:** Coming soon...

### VII. Nodal analysis 
**Level 1 Nodal Analysis:** Consider the following circuit:
![Level 1 nodal circuit](/btg_nodalLevel1.svg)
*<center>Level 1 nodal analysis circuit example</center>*
This circuit has three nodes and leads to an analysis with three equations and three unknowns. Note that the $5\text{V}$ voltage source $V_S$ gives a constraint equation. First, we define the voltages at the 'top' of the circuit with respect to the directions indicated in the figure. The constraint equation gives:
$$V_1 = 5\text{V}.$$

The next equation can be obtained by applying Kirchhoff's current law (KCL) at node defined by $V_2$. The approach is to sum the currents entering and equate them to the sum of currents leaving. The mechanics of this technique can be developed differently. The solution here uses the 'currents leaving' the node $V_2$ as the starting point and the 'currents entering' the node $V_2$ as current sources (like $I_S$). The resulting KCL equation gives

$$\begin{align}\sum I_\text{Leaving} &= \sum I_\text{Entering} \newline
I_{R1} + I_{R2} &= I_S \newline
\frac{V_2-V_1}{R_1} + \frac{V_2-V_3}{R_2} &= I_S \newline
\frac{-V_1}{R_1} + V_2\Bigg(\frac{1}{R1}+\frac{1}{R2}\Bigg) + \frac{-V_3}{R_2} &= I_S \newline
 -0.5m\mho V_1 + 1.5m\mho V_2 - 1m\mho V_3&= 20mA\newline
  -0.5V_1 + 1.5V_2 - 1V_3&= 20.\end{align}$$.
  
  The final node $V_3$ gives the third equation needed:
  $$\begin{align}\sum I_\text{Leaving} &= \sum I_\text{Entering} \newline
I_{R2} + I_{R3} &= 0 \newline
\frac{V_3-V_2}{R_2} + \frac{V_3}{R_3} &= 0 \newline
\frac{-V_2}{R_2} + V_3\Bigg(\frac{1}{R_2}+\frac{1}{R_3}\Bigg) &= 0 \newline
-1m\mho V_2 + 1.333m\mho V_3 &= 0 \newline
-1 V_2 + 1.333 V_3 &= 0.
\end{align}$$.

The resulting system of equations is

$$
\begin{bmatrix}
1 & 0 & 0 \newline
-0.5 & 1.5 & -1 \newline
0 & -1 & 1.333 
\end{bmatrix}
\begin{bmatrix}
V_1 \newline
V_2 \newline
V_3
\end{bmatrix}  =
\begin{bmatrix}
5 \newline
20 \newline
0
\end{bmatrix}
$$

which gives the solution $V_1=5V$, $V_2=30V$, and $V_3=22.5V$.

**Level 2 Nodal Analysis:** Consider the following circuit:
![Level 2 nodal circuit](/btg_nodalLevel2a.svg)
*<center>Level 2 nodal analysis circuit example</center>*
This circuit has five nodes and could to an analysis with five equations and five unknowns. In order to simplify the problem, note that there are two voltage sources that may be used to solve for nodes corresponding to $V_{S1}=5V$ and $V_{S2}=3V$. From this point, the following analysis will substitue these values in order to reduce the circuit analysis to involve three equations and three unknowns. First, we define the voltages at the 'top' of the circuit with respect to the directions indicated in the figure. 

The next equation can be obtained by applying Kirchhoff's current law (KCL) at node defined by $V_1$. The approach is to sum the currents entering and equate them to the sum of currents leaving. The resulting KCL equation gives

$$\begin{align}\sum I_\text{Leaving} &= \sum I_\text{Entering} \newline
I_{R1} + I_{R2} + I_{R5} &= 0 \newline
\frac{V_1-V_{S1}}{R_1} + \frac{V_1-V_2}{R_2} + \frac{V_1-V_{S2}}{R_5} &= 0 \newline
V_1\Bigg(\frac{1}{R_1}+\frac{1}{R_2}+\frac{1}{R_5} \Bigg) - \frac{V_2}{R_2} - \frac{V_{S1}}{R_1} - \frac{V_{S2}}{R_5} &= 0 \newline
\end{align}$$.

Considering the intent of expressing this equation later in a system, it may be rearranged to move the constants to one side.

$$\begin{align}
V_1\Bigg(\frac{1}{R_1}+\frac{1}{R_2}+\frac{1}{R_5} \Bigg) - \frac{V_2}{R_2} &=  \frac{V_{S1}}{R_1} + \frac{V_{S2}}{R_5} \newline
7.5m\mho V_1 - 2m\mho V_2 &= 2.5mA + 15mA \newline
7.5 V_1 - 2 V_2 &= 17.5 \newline
\end{align}$$.

The next equation can be obtained by applying Kirchhoff's current law (KCL) at node defined by $V_2$.
$$\begin{align}\sum I_\text{Leaving} &= \sum I_\text{Entering} \newline
I_{R2} + I_{R3} &= 20mA \newline
\frac{V_2-V_{1}}{R_2} + \frac{V_2-V_3}{R_3} &= 20mA \newline
-\frac{V_1}{R_2} + V_2\Bigg( \frac{1}{R_2}+\frac{1}{R_3}\Bigg) - \frac{V_3}{R_3} &= 20mA \newline
-2m\mho V_1 + 3m\mho V_2 -1m\mho V_3 &= 20mA \newline
-2V_1 + 3V_2 - V_3 &= 20
\end{align}$$.

The final equation can be obtained by applying Kirchhoff's current law (KCL) at node defined by $V_3$.
$$\begin{align}\sum I_\text{Leaving} &= \sum I_\text{Entering} \newline
I_{R3} + I_{R4} &= 0A \newline
\frac{V_3-V_2}{R_3} + \frac{V_3}{R_4} &= 0A \newline
-\frac{V_2}{R_3} + V_3\Bigg( \frac{1}{R_3} + \frac{1}{R_4} \Bigg) &= 0A \newline
-1m\mho V_2 + 1.333m\mho V_3 &= 0A \newline
-V_2 + 1.333V_3 &= 0 \newline
\end{align}$$.

The resulting system of equations is

$$
\begin{bmatrix}
7.5 & -2 & 0 \newline
-2 & 3 & -1 \newline
0 & -1 & 1.333 
\end{bmatrix}
\begin{bmatrix}
V_1 \newline
V_2 \newline
V_3
\end{bmatrix}  =
\begin{bmatrix}
17.5 \newline
20 \newline
0
\end{bmatrix}
$$

which gives the solution $V_1=6.165V$, $V_2=14.369V$, and $V_3=10.777V$.

**Level 3 Nodal Analysis:** Coming soon...


### VIII. Voltage dividers and current dividers 
### IX. Series and parallel elements 
### X. Thévenin & Norton equivalent circuits 
### XI. Energy storage elements

|	  | ![Capacitor](/btg_capacitorDef.svg)				|   | ![Inductor](/btg_inductorDef.svg)				|
|--- 	  | --- 							|---| --- 							|
|	  | **Capacitance - Farads [F]**				|   | **Inductor - Henries [H]**					|
|Field	  | Electric							|   |Magnetic							|
|Current  |$i_C(t)=\frac{dq}{dt}=C\frac{dv_C(t)}{dt}$			|   |$i_L(t)= i_L(t_0)+\frac{1}{L}\int_{t_0}^t v_L(\tau)d\tau$ 	|
|Voltage  |$v_C(t)= v_C(t_0)+\frac{1}{C}\int_{t_0}^t i_C(\tau)d\tau$  	|   |$v_L=L\frac{di_L(t)}{dt}$					|
|Energy	  |$E_C=\frac{1}{2}Cv_C^2(t)$					|   |$E_L=\frac{1}{2}Li_L^2(t)$					|
|Impedance|$Z_C=\frac{1}{j\omega C}=\frac{1}{sC}$			|   |$Z_L=j\omega L=sL$				|	
|Series	 |$C_\text{Eq}=\big( \frac{1}{C_1} + \frac{1}{C_2} + \dots + \frac{1}{C_n}\big)^{-1}$						|  |$L_\text{Eq} = L_1+L_2+\dots+L_n$								|
|Parallel|$C_\text{Eq} = C_1+C_2+\dots+C_n$			|   |$L_\text{Eq}=\big( \frac{1}{L_1} + \frac{1}{L_2} + \dots + \frac{1}{L_n}\big)^{-1}$								|
|Symobls  | ![Capacitor Symbols](/btg_capacitorSchematics.svg)		|   |![Capacitor Symbols](/btg_inductorSchematics.svg)		| 
### XII. Time-domain solutions for transient RC circuits 

$$f(t)=\frac{d}{dt}f(t)$$

where $f(0) = 1$ (*note: if $f(0)=0$ nothing intersting happens*).

$$\begin{align}
f(t) 	     &=&1         &&+	    &&t		&&+	  &&\frac{t^2}{2}&&+	   &&\frac{t^3}{3\cdot2}&&+	  &&\frac{t^4}{4\cdot3\cdot2\cdot1}&&+ \dots + \frac{t^n}{n!}	\newline
     	     & &\downarrow&&\nearrow&&\downarrow&&\nearrow&&\downarrow   &&\nearrow&&\downarrow		&&\nearrow&&\downarrow	&&\newline
f'(t)	     &=&1	  &&+	    &&t		&&+	  &&\frac{t^2}{2}&&+	   &&\frac{t^3}{3\cdot2}&&+	  &&\frac{t^4}{4\cdot3\cdot2\cdot1}&&+ \dots + \frac{t^n}{n!}
\end{align}$$

$$f(t) = \sum_0^\infty \frac{t^n}{n!} = e^t$$



### XIII. Laplace transforms (notions for frequency-domain RC circuits) 
### XIV. Complex numbers, rational polynomials, sinusoids, magnitude & phase

Imaginary numbers enable analysis of oscillations by linking a simple exponential function to sine and cosine functions. This is important because when designing electronic systems, arbitrary signals will be modeled as a summation of sine and cosine functions. When manipulating these signals the equivalent exponential expression will offer a compact and convienent form that can carry insight in both time and frequency domain analysis. $j=\sqrt{-1}$, $j^2 = -1$, $-j = \frac{1}{j}$
$$\frac{1}{j} = \frac{1}{j}\frac{j}{j} = \frac{j}{-1} = -j$$
$$a+jb = Re^{j\theta} = R\angle \theta$$
$$ \theta = \text{tan}^{-1}\bigg(\frac{b}{a}\bigg)$$
$$ \theta = -j\text{ln}\bigg(\frac{a+jb}{R}\bigg)$$
$$H = \frac{a+jb}{c+jd} = \frac{R_1e^{j\theta_1}}{R_2e^{j\theta_2}} $$
$$|H| = \Bigg|\frac{a+jb}{c+jd}\Bigg|=\frac{|a+jb|}{|c+jd|} = \frac{R_1}{R_2} $$
$$\angle(H) =\angle\Bigg(\frac{R_1e^{j\theta_1}}{R_2e^{j\theta_2}}\Bigg) = \angle\Bigg(\frac{R_1e^{j\theta_1}e^{-j\theta_2}}{R_2}\Bigg) = \angle\Bigg(\frac{R_1}{R_2}e^{j(\theta_1-\theta_2)}\Bigg) =\theta_1 - \theta_2$$

Changing angles as a function of time leads to concepts like angular velocity, frequency and period. Complex exponentials provide a compact notation for sinusoidal waveforms. This can be proven by several approaches. Valuable intuition can be outlined through the development of $e^t$ as an 'eigenfunction' for differential operators and Taylor's series expansions.

$$e^{\pm j \pi} = e^{\pm j 180^o} = -1$$

$$e^{j\omega t} = \text{cos}(\omega t) + j \text{sin}(\omega t)$$

$$e^{j\omega \pi} = \text{cos}(\omega \pi) + j \text{sin}(\omega \pi)$$

$$e^{j\omega \pi} - 1 = 0$$

$$e^{j\omega t + \phi} = \text{cos}(\omega t + \phi) + j \text{sin}(\omega t + \phi)$$

A Taylor series is an expansion of a function that results in infinite terms defined by the function's derivative. The result gives a representation of a function at and around a point. Considering a finite amount of terms, the abbreviated expansion approximates the original function a and around a point. This approximation becomes more accurate as more terms in the series are considered. The definition of the Taylor series is

$$\begin{align}
f(t)|_{t=a}&=f(a)+\frac{f'(a)}{1!}(t-a)+\frac{f''(a)}{2!}(t-a)^2+\frac{f'''(a)}{3!}(t-a)^3+\dots \newline
&=\sum_0^\infty\frac{f^{(n)}(a)}{n!}(t-a)^n.
\end{align}$$ 

As a result, the function $f(t)$ can be approximated at (and around) point $a$ to an accuracy related to the amount of summation terms. Applying this expansion at the point $a=0$ is called the Maclaurin series. By keeping a the partial sum (as opposed to infinite summation terms) results in an approximation to a polynomical degree $k$ where the $k^\text{th}$ term is the highest term retained in the summation. This treatment is often referred to as approximating a function to the $k^\{th}$ order. For example, approximating $f(t)$ to the 'zeroth order' implies keeping $k=0$ summation terms to represents $f(t)$ as a constant at point $t=a$ and gives a poor approximation of the function as points 'away' from $a$ are considered. Likewise, approximating $f(t)$ to the 'first order' implies keeping $k=1$ to represent $f(t)$ as a line that passes through point $t=a$ and gives a slightly better approximation of the function as points 'away' from $a$ are considered. Similarly, approximating $f(t)$ to the 'second order' can improve approximations by using quadradtic functions, and so on.

$$\begin{align}
e^{j\omega t}|_{t=0}&=f(a)+\frac{f'(a)}{1!}(t-a)+\frac{f''(a)}{2!}(t-a)^2+\frac{f'''(a)}{3!}(t-a)^3+\dots \newline
&=e^{0}+j\omega e^0 t+\frac{(j\omega)^2 e^0}{2} t^2+\frac{(j\omega)^3 e^0}{6} t^3+\frac{(j\omega)^4 e^0}{24} t^4+\dots \newline
&=1+j\omega t+\frac{(j\omega)^2}{2} t^2+\frac{(j\omega)^3}{6} t^3+\frac{(j\omega)^4}{24} t^4+\dots
\end{align}$$ 


$$\begin{align}
\text{cos}(\omega t)|_{t=0}&=f(a)+\frac{f'(a)}{1!}(t-a)+\frac{f''(a)}{2!}(t-a)^2+\frac{f'''(a)}{3!}(t-a)^3+\dots \newline
&= \text{cos}(0) - \omega\text{sin}(0)t - \frac{\omega^2}{2}\text{cos}(0)t^2 + \frac{\omega^3}{6}\text{sin}(0)t^3 + \frac{\omega^4}{24}\text{cos}(0)t^4 + \dots \newline
&= 1 - \frac{\omega^2}{2}t^2 + \frac{\omega^4}{24}t^4 - \frac{\omega^6}{720}t^6 + \dots 
\end{align}$$ 


$$\begin{align}
\text{sin}(\omega t)|_{t=0}&=f(a)+\frac{f'(a)}{1!}(t-a)+\frac{f''(a)}{2!}(t-a)^2+\frac{f'''(a)}{3!}(t-a)^3+\dots \newline
&=\text{sin}(0) + \omega\text{cos}(0)t + \frac{\omega^2}{2}\text{sin}(0)t^2 - \frac{\omega^3}{6}\text{cos}(0)t^3 - \frac{\omega^4}{24}\text{cos}(0)t^4 + \dots \newline
&= 0 + \omega t - \frac{\omega^3}{6}t^3 + \frac{\omega^5}{120}t^5 + \dots
\end{align}$$ 

Considering the point $a=0$, the Taylor series expressions for $\text{cos}(\omega t)$ and $\text{sin}(\omega t)$ can be combined and rearranged to form the Taylor series expansion for $e^{j\omega t}$ as follows:

$$\begin{align}
e^{j\omega t} &= \text{cos}(\omega t) + j\text{sin}(\omega t) \newline
&= \bigg( 1 - \frac{\omega^2}{2}t^2 + \frac{\omega^4}{24}t^4 - \frac{\omega^6}{720}t^6 + \dots  \bigg) + j\bigg( \omega t - \frac{\omega^3}{6}t^3 + \frac{\omega^5}{120}t^5 + \dots \bigg) \newline
&= 1 - \frac{\omega^2}{2}t^2 + \frac{\omega^4}{24}t^4 - \frac{\omega^6}{720}t^6 + j\omega t - j\frac{\omega^3}{6}t^3 + j\frac{\omega^5}{120}t^5 + \dots \newline
&= 1 + j\omega t - \frac{\omega^2}{2}t^2 - j\frac{\omega^3}{6}t^3 + \frac{\omega^4}{24}t^4 + j\frac{\omega^5}{120}t^5 - \frac{\omega^6}{720}t^6 + \dots \newline
&= 1 + j\omega t + \frac{(j\omega)^2}{2}t^2 + \frac{(j\omega)^3}{6}t^3 + \frac{(j\omega)^4}{24}t^4 + \frac{(j\omega)^5}{120}t^5 + \frac{(j\omega)^6}{720}t^6 + \dots \newline
&= \frac{1}{0!} + \frac{j\omega}{1!}t + \frac{(j\omega)^2}{2!}t^2 + \frac{(j\omega)^3}{3!}t^3 + \frac{(j\omega)^4}{4!}t^4 + \frac{(j\omega)^5}{5!}t^5 + \frac{(j\omega)^6}{6!}t^6 + \dots \newline
&=\sum_0^\infty\frac{(j\omega)^n}{n!}(t)^n \newline
&=\sum_0^\infty\frac{f^{(n)}(a)}{n!}(t-a)^n.
\end{align}$$

### XV. Log functions, decibels and their plots 
The compounding nature of exponential growth allows exponential functions can magnify errors, perturbations or changes. This means points that are nearby may be 'stretched' or expanded away from one another by the action of a the funciton $e^t$. The inverse is true for logarithmic functions. Logarithmic functions 'squish' or compress distant points by an action that tends to normalize vast scales into a new... 

### XVI. Simple RC filters 


[^fn1]: Irwin, J. D., & Nelms, R. M. (2020). *Basic engineering circuit
[^fn2]: Swokowski, E. W., & Cole, J. A. (2012). Algebra and trigonometry with analytic geometry. Cengage Learning.
[^fn3]: Lathi, B. P., & Green, R. A. (1998). Signal processing and linear systems. Oxford: Oxford University Press.
