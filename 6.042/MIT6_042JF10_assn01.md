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
