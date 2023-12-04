<h1 align="center" >Chapter 1 : Programming General Overview</h1>

# Contents :

### 1. Mathematical Review

### 2. Brief Introduction to Recursion

### 3. Classes

### 4. Details

### 5. Templates

### 6. Using Matrices

---

<h1 align="center" >1. Mathematical Review</h1>

#### <p align="center" >This section lists some of the basic formulas you need to memorize, or be able to derive, and reviews basic proof techniques.</p>

### 1.1 Exponents

1. ### <p>$$\ X^AX^B = X^{A+B} $$</p>

2. ### <p>$$\ {X^A \over X^B} = X^{A-B} $$</p>

3. ### <p>$$\ (X^A)^B = X^{AB} $$</p>

4. ### <p>$$\ X^N + X^N = 2X^N \ne X^2N $$</p>

5. ### <p>$$\ 2^N + 2^N = 2^{N+1} $$</p>

### 1.2 Logarithms

#### In computer science, all logarithms are to the base 2 unless speciﬁed otherwise.

#### Definition :

### <p>$${X^A = B} \ \ if \ and \ only \ if \log_{X}B = A $$</p>

---

#### Theorem :

### <p>$\ \log_AB = {\log {c}B \over \log_cA}; \ A,B,C > 0, \ A \ne 1 $</p>

#### Proof :

### <p>$$Let\ X=\log_{C}B$$</p>

### <p>$$Y=\log_{C}A,$$</p>

### <p>$$and\ Z=\log_{A}B$$</p>

### <p>$$Then\ By\ The\ Definition\ Of\ Logarithms\ ,$$</p>

### <p>$$C^X = B,$$</p>

### <p>$$C^Y = A$$</p>

### <p>$$and\ A^Z = B$$</p>

### <p>$$Combining\ these\ three\ equalities\ yields$$</p>

### <p>$$B = C^X = (C^Y)^Z$$</p>

### <p>$$Therefore,\ X=YZ$$</p>

### <p>$$Which\ Implies,\ {Z=X \over Y}$$</p>

### <p>$$Proving\ The\ Theorem$$</p>

---

#### Theorem :

### <p>$\ \log AB = {\log A + \log B}; \ A,B > 0 $</p>

#### Proof :

### <p>$$Let\ X=\log A$$</p>

### <p>$$Y=\log B,$$</p>

### <p>$$and\ Z=\log AB$$</p>

### <p>$$Then,\ assuming\ the\ default\ base\ of\ 2 ,$$</p>

### <p>$$2^X = A$$</p>

### <p>$$2^Y = B$$</p>

### <p>$$and\ 2^Z = AB$$</p>

### <p>$$Combining\ the\ last\ three\ equalities\ yields$$</p>

### <p>$$2^X2^Y = AB = 2^Z$$</p>

### <p>$$Therefore,\ X + Y = Z$$</p>

### <p>$$which\ Proves\ The\ Theorem$$</p>

---

#### Some other useful formulas, which can all be derived in a similar manner, follow.

1. ### <p>$$\log {A / B} = \log A - \log B $$</p>
1. ### <p>$$\log {(A)}^B = B\log A$$</p>
1. ### <p>$$\log X < X\ for\ all\ X > 0$$</p>

### <p>$$\log 1 = 0\ \ \ \ \ ,\log 2 = 1\ \ \ \ \ ,\log 1,024 = 10\ \ \ \ \ ,\log 1,048,576 = 20 $$</p>

### 1.3 Series

#### <p align="center" >The easiest formulas to remember are</p>

### <p>$$\sum_{i=0}^N 2^i = 2^{N+1}-1$$</p>

#### <p align="center" >and the companion,</p>

### <p>$$\sum_{i=0}^N A^i = {A^{N+1} - 1 \over A - 1}$$</p>

### <p align="center" >In the latter formula, if 0 < A < 1 , then</p>

### <p>$$\sum_{i=0}^N A^i \leq {1 \over A - 1} $$</p>

#### <p>and as N tends to ∞, the sum approaches 1/(1 − A). These are the “geometric series” formulas. We can derive the last formula $\sum_{i=0}^∞ A^i (0 < A < 1)$ in the following manner. Let S be the sum. Then</p>

#### <p align="center">S = 1 + A + A2 + A3 + A4 + A5 + · · ·</p>

#### Then

#### <p align="center">AS = A + A2 + A3 + A4 + A5 + · · ·</p>

#### <p>If we subtract these two equations (which is permissible only for a convergent series), virtually all the terms on the right side cancel, leaving $$S-AS=1$$ which implies that $$S={1 \over {1-A}}$$</p>

#### <p>We can use this same technique to compute $\sum_{i=1}^∞{i \over 2^i},$ a sum that occurs frequently.<br/> We write</p>

#### <p>$$S = {1 \over 2} + {2 \over 2^2} + {3 \over 2^3} + {4 \over 2^4} +{5 \over 2^5} +\ ·\ ·\ · $$ and multiply by 2, obtaining</p>

#### <p>$$2S = 1 + {2 \over 2} + {3 \over 2^2} + {4 \over 2^3} +{5 \over 2^4} + {6 \over 2^5}\ ·\ ·\ · $$ Subtracting these two equations yields</p>

#### <p>$$S = 1 + {1 \over 2} + {1 \over 2^2} + {1 \over 2^3} +{1 \over 2^4} + {1 \over 2^5}\ ·\ ·\ · $$ Thus, S = 2.</p>

#### <p>Another type of common series in analysis is the arithmetic series. Any such series can be evaluated from the basic formula: $$\sum_{i=1}^N = {N(N+1) \over 2} ≈ {N^2 \over 2} $$</p>

#### <p>For instance, to ﬁnd the sum 2 + 5 + 8 + · · · + (3k − 1), rewrite it as 3(1 + 2 + 3 +· · · + k) − (1 + 1 + 1 + · · · + 1), which is clearly 3k(k + 1)/2 − k. Another way to remember this is to add the ﬁrst and last terms (total 3k + 1), the second and next-to-last terms (total 3k + 1), and so on. Since there are k/2 of these pairs, the total sum is k(3k + 1)/2, which is the same answer as before.<br/>The next two formulas pop up now and then but are fairly uncommon.$$\sum_{i=1}^N = {N(N+1)(2N+1) \over 6} ≈ {N^3 \over 3}$$ $$\sum_{i=1}^Ni^K ≈ {N^{K+1} \over |K+1|} K \ne -1 $$</p>

#### <p>When k = −1, the latter formula is not valid. We then need the following formula, which is used far more in computer science than in other mathematical disciplines. The numbers HN are known as the harmonic numbers, and the sum is known as a harmonic sum. The error in the following approximation tends to γ ≈ 0.57721566, which is known as Euler’s constant $$H_N = \sum_{i=1}^N{1 \over i} ≈ \log_{e}N $$</p>

#### <p>These two formulas are just general algebraic manipulations: $$\sum_{i=1}^Nf(N)=Nf(N)$$ $$\sum_{i=n_0}^Nf(i)=\sum_{i=1}^Nf(i)-\sum_{i=1}^{n_0-1}f(i) $$</p>

### 1.4 Modular Arithmetic

#### <p>We say that A is congruent to B modulo N, written A ≡ B (mod N), if N divides A − B. Intuitively, this means that the remainder is the same when either A or B is divided by N. Thus, 81 ≡ 61 ≡ 1 (mod 10). As with equality, if A ≡ B (mod N), then A + C ≡ B + C (mod N) and AD ≡ BD (mod N).<br/><br/><br/>Often, N is a prime number. In that case, there are three important theorems:<br/><br/>$\qquad$ First, if N is prime, then ab ≡ 0 (mod N) is true if and only if a ≡ 0 (mod N) or b ≡ 0 (mod N). In other words, if a prime number N divides a product of two numbers, it divides at least one of the two numbers.<br/> $\qquad$ Second, if N is prime, then the equation ax ≡ 1 (mod N) has a unique solution (mod N) for all 0 < a < N. This solution, 0 < x < N, is the multiplicative inverse.<br/> $\qquad$ Third, if N is prime, then the equation x2 ≡ a (mod N) has either two solutions (mod N) for all 0 < a < N, or it has no solutions<br/><br/>$\qquad$ There are many theorems that apply to modular arithmetic, and some of them require extraordinary proofs in number theory. We will use modular arithmetic sparingly, and the preceding theorems will sufﬁce.</p>

### 1.5 The P Word

<h1 align="center" >2. Brief Introduction to Recursion</h1>

<h1 align="center" >3. Classes</h1>

<h1 align="center" >4. Details</h1>

<h1 align="center" >5. Templates</h1>

<h1 align="center" >6. Using Matrices</h1>
