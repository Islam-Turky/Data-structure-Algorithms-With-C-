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

### <p align="center" >In the latter formula, if $$0 < A < 1$$ , then</p>

### <p>$$\sum_{i=0}^N A^i \leq {1 \over A - 1} $$</p>

#### <p>and as N tends to ∞, the sum approaches 1/(1 − A). These are the “geometric series” formulas. We can derive the last formula $$\sum_{i=0}^∞ A^i (0 < A < 1)$$ in the following manner. Let S be the sum. Then</p>

#### <p align="center">S = 1 + A + A2 + A3 + A4 + A5 + · · ·</p>

#### Then

#### <p align="center">AS = A + A2 + A3 + A4 + A5 + · · ·</p>

### 1.4 Modular Arithmetic

### 1.5 The P Word

<h1 align="center" >2. Brief Introduction to Recursion</h1>

<h1 align="center" >3. Classes</h1>

<h1 align="center" >4. Details</h1>

<h1 align="center" >5. Templates</h1>

<h1 align="center" >6. Using Matrices</h1>
