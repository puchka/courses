# Problem Set 1

## Problem 1. [24 points]

Translate the following sentences from English to predicate logic. The domain that you are
working over is $X$, the set of people. You may use the functions $S(x)$, meaning that “x has
been a student of 6.042,” $A(x)$, meaning that “x has gotten an ‘A’ in 6.042,” $T(x)$, meaning
that “x is a TA of 6.042,” and $E(x, y)$, meaning that “x and y are the same person.”

(a) [6 pts] There are people who have taken 6.042 and have gotten A’s in 6.042

$$
\exists x \in X, S(x) ~and~ A(x).
$$

(b) [6 pts] All people who are 6.042 TA’s and have taken 6.042 got A’s in 6.042

$$
\forall x \in X, T(x) ~and~ S(x) \implies A(x).
$$

(c) [6 pts] There are no people who are 6.042 TA’s who did not get A’s in 6.042.

$$
\forall x \in X, T(x) \iff A(x).
$$

(d) [6 pts] There are at least three people who are TA’s in 6.042 and have not taken 6.042

$$
\exists x, y, z \in X, x \neq y ~and~ y \neq z ~and~ x \neq z ~and~ T(x) ~and~ T(y) ~and~ T(z) ~and~ \neg S(x) ~and~ \neg S(y) ~and~ \neg S(z)
$$

## Problem 2. [24 points]

Use a truth table to prove or disprove the following statements:

(a) [12 pts]

$$
\neg (P \lor (Q \land R)) = (\neg P) \land (\neg Q \lor \neg R)
$$

\begin{tabular}{|c|c|c|c|c|c|c|c|c|c|c|c|}
$P$ & $Q$ & $R$ & $Q \land R$ & $P \lor (Q \land R)$ & $\neg (P \lor (Q \land R))$ & $\neg P$ & $\neg Q$ & $\neg R$ & $\neg Q \lor \neg R$ & $(\neg P) \land (\neg Q \lor \neg R)$ \\
\hline
$T$ & $T$ & $T$ & $T$         & $T$                  & $F$                         & $F$      & $F$      & $F$      & $F$                  & $F$ \\
$T$ & $T$ & $F$ & $F$         & $T$                  & $F$                         & $F$      & $F$      & $T$      & $T$                  & $F$ \\
$T$ & $F$ & $T$ & $F$         & $T$                  & $F$                         & $F$      & $T$      & $F$      & $T$                  & $F$ \\
$T$ & $F$ & $F$ & $F$         & $T$                  & $F$                         & $F$      & $T$      & $T$      & $T$                  & $F$ \\
$F$ & $T$ & $T$ & $T$         & $T$                  & $F$                         & $T$      & $F$      & $F$      & $F$                  & $F$ \\
$F$ & $T$ & $F$ & $F$         & $F$                  & $T$                         & $T$      & $F$      & $T$      & $T$                  & $T$ \\
$F$ & $F$ & $T$ & $F$         & $F$                  & $T$                         & $T$      & $T$      & $F$      & $T$                  & $T$ \\
$F$ & $F$ & $F$ & $F$         & $F$                  & $T$                         & $T$      & $T$      & $T$      & $T$                  & $T$ \\
\end{tabular}

According to the truth table above

$$
\neg (P \lor (Q \land R)) = (\neg P) \lor (\neg Q \lor \neg R)
$$

(b) [12 pts]

$$
\neg (P \land (Q \lor R)) = \neg P \lor (\neg Q \lor \neg R)
$$

\begin{tabular}{|c|c|c|c|c|c|c|c|c|c|c|c|}
$P$ & $Q$ & $R$ & $Q \land R$ & $P \lor (Q \land R)$ & $\neg (P \lor (Q \land R))$ & $\neg P$ & $\neg Q$ & $\neg R$ & $\neg Q \lor \neg R$ & $\neg P \lor (\neg Q \lor \neg R)$ \\
\hline
$T$ & $T$ & $T$ & $T$         & $T$                  & $F$                         & $F$      & $F$      & $F$      & $F$                  & $F$ \\
$T$ & $T$ & $F$ & $F$         & $T$                  & $F$                         & $F$      & $F$      & $T$      & $T$                  & $T$ \\
$T$ & $F$ & $T$ & $F$         & $T$                  & $F$                         & $F$      & $T$      & $F$      & $T$                  & $T$ \\
$T$ & $F$ & $F$ & $F$         & $T$                  & $F$                         & $F$      & $T$      & $T$      & $T$                  & $T$ \\
$F$ & $T$ & $T$ & $T$         & $T$                  & $F$                         & $T$      & $F$      & $F$      & $F$                  & $T$ \\
$F$ & $T$ & $F$ & $F$         & $F$                  & $T$                         & $T$      & $F$      & $T$      & $T$                  & $T$ \\
$F$ & $F$ & $T$ & $F$         & $F$                  & $T$                         & $T$      & $T$      & $F$      & $T$                  & $T$ \\
$F$ & $F$ & $F$ & $F$         & $F$                  & $T$                         & $T$      & $T$      & $T$      & $T$                  & $T$ \\
\end{tabular}

According to the truth table above

$$
\neg (P \lor (Q \land R)) \neq \neg P \lor (\neg Q \lor \neg R)
$$

## Problem 3. [24 points]

The binary logical connectives $\land$ (and), $\lor$ (or ), and $\implies$ (implies) appear often in not only
computer programs, but also everyday speech. In computer chip designs, however, it is
considerably easier to construct these out of another operation, $nand$, which is simpler to
represent in a circuit. Here is the truth table for $nand$:

\begin{tabular}{|c|c|c|}
$P$     & $Q$     & $P ~nand~ Q$ \\
\hline
$true$  & $true$  & $false$ \\
$true$  & $false$ & $true$  \\
$false$ & $true$  & $true$  \\
$false$ & $false$ & $true$  \\
\end{tabular}

a) [12 pts] For each of the following expressions, find an equivalent expression using only
nand and $\neg$ (not), as well as grouping parentheses to specify the order in which the operations
apply. You may use $A$, $B$, and the operators any number of times.


(i) $A \land B$

\begin{tabular}{|c|c|c|c|c|}
$A$ & $B$ & $A \land B$ & $A ~nand~ B$ & $\neg (A ~nand~ B)$ \\
\hline
$T$ & $T$ & $T$         & $F$          & $T$                 \\
$T$ & $F$ & $F$         & $T$          & $F$                 \\
$F$ & $T$ & $F$         & $T$          & $F$                 \\
$F$ & $F$ & $F$         & $T$          & $F$                 \\
\end{tabular}

$$
A \land B = \neg (A ~nand~ B)
$$

(ii) $A \lor B$

\begin{tabular}{|c|c|c|c|c|c|}
$A$ & $B$ & $A \lor B$  & $\neg A$ & $\neg B$ & $\neg A ~nand~ \neg B$ \\
\hline
$T$ & $T$ & $T$         & $F$      & $F$      & $T$                  \\
$T$ & $F$ & $T$         & $F$      & $T$      & $T$                  \\
$F$ & $T$ & $T$         & $T$      & $F$      & $T$                  \\
$F$ & $F$ & $F$         & $T$      & $T$      & $F$                  \\
\end{tabular}

$$
A \lor B = \neg A ~nand~ \neg B
$$

(iii) $A \implies B$


\begin{tabular}{|c|c|c|c|c|c|c|}
$A$ & $B$ & $A \implies B$  & $\neg A$ & $\neg A \lor B$ & $\neg B$ & $A ~nand~ \neg B$ \\
\hline
$T$ & $T$ & $T$             & $F$      & $T$             & $F$      & $T$               \\
$T$ & $F$ & $F$             & $F$      & $F$             & $T$      & $F$               \\
$F$ & $T$ & $T$             & $T$      & $T$             & $F$      & $T$               \\
$F$ & $F$ & $T$             & $T$      & $T$             & $T$      & $T$               \\
\end{tabular}

$$
A \implies B = A ~nand~ \neg B
$$

b) [4 pts] It is actually possible to express each of the above using only nand, without
needing to use $\neg$. Find an equivalent expression for $(\neg A)$ using only nand and grouping
parentheses.

\begin{tabular}{|c|c|c|}
$A$ & $\neg A$ & $A ~nand~ A$ \\
\hline
$T$ & $F$      & $F$          \\
$F$ & $T$      & $T$          \\
\end{tabular}

$$
\neg A = A ~nand~ A
$$

(c) [8 pts] The constants $true$ and $false$ themselves may be expressed
using only $nand$.  Construct an expression using an arbitrary statement
$A$ and $nand$ that evaluates to $true$ regardless of whether $A$ is $true$ or
$false$. Construct a second expression that always evaluates to
$false$. Do not use the constants $true$ and $false$ themselves in your
statements.

First let's devise a tautology i.e an expression that is always true
regardless of its component.

One example of tautology is $A \lor \neg A$

We previously saw that:

$$
A \lor B = \neg A ~nand~ \neg B
$$

$$
A \lor \neg A = \neg A ~nand~ A ~with~ B = \neg A ~and~ \neg \neg A = A
$$

$$
A \lor \neg A = (A ~nand~ A) ~nand~ A ~as~ \neg A = A ~nand~ A
$$

So, $(A ~nand~ A) ~nand~ A$ is an expression that always evaluate to
$true$ whether $A$ is $true$ or $false$.

On the other hand, a contradiction is a statement that is always
$false$, regardless of the truth values of its individual
components.

For example, the statement $A \land \neg A$ is a contradiction because it
is always $false$, no matter the truth value of $A$.

As we previously saw,


$$
A \land B = \neg (A ~nand~ B)
$$

With $B = \neg A$

$$
A \land \neg A = \neg (A ~nand~ \neg A)
$$

With $\neg A = A ~nand~ A$

$$
A \land \neg A = (A ~nand~ (A ~nand~ A)) ~nand~ (A ~nand~ (A ~nand~ A))
$$

We can conclude that $(A ~nand~ (A ~nand~ A)) ~nand~ (A ~nand~ (A
~nand~ A))$ is an expression that is always ~false~ regardless of the
truth value of $A$.

## Problem 4. [10 points]

You have 12 coins and a balance scale, one of which is fake. All
the real coins weigh the same, but the fake coin weighs less than the rest. All the coins
visually appear the same, and the difference in weight is imperceptible to your senses. In at
most 3 weighings, give a strategy that detects the fake coin. (Note: the scale in this problem
is a scale with two dishes, which tips toward the side that is heavier. For clarification, do an
image search for “balance scale”).

1) Devide the coins in 2 sets of 6 coins each, the fake coin will be among the ones that are up.
2) Devide those in 2 sets of 3 coins each, the fake coin will be among those which are collectively lighter.
3) Among the remaining 3, pick two and compare their weight.
   - If they are the same weight, the one you didn't pick is the fake one.
   - Otherwhise, if one of them is lighter, it's the fake coin.
