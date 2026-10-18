# Finite Geometry & Linear Algebra in Combinatorics — EGMO Camp

Oct 18, 2026 · @Someone

## Overview

Two hours is enough for one complete lecture, so this is split into two: Lecture 1 builds finite projective planes and uses them in counting problems, and Lecture 2 (next month) adds linear algebra over F₂ as a combinatorial tool. Lecture 1 stands on its own if the second session falls through.

**Prerequisites:** modular arithmetic, basic double counting, and vectors (x, y, z) with the dot product. No prior linear algebra is needed for Lecture 1.

**Classroom setup for 30 students:**

- Groups of 3–4 (about 8 tables), each mixing stronger and weaker students.
- Problems are tagged ★ (everyone), ★★ (most groups) and ★★★ (top students), so fast groups always have something to do.
- Each lecture ends with groups presenting solutions at the board, which doubles as proof-writing practice.

**Materials:** a Spot It (Dobble) deck if you can get one, printed Fano plane diagrams, and the problem sheets below.

## Lecture 1: Geometry with finitely many points

Students discover the Fano plane through a card game, prove the basic counting theorem, then build projective planes from coordinates over F\_q and use them on extremal problems.

| Time | Segment | What happens |
| --- | --- | --- |
| 0:00–0:10 | Hook: Spot It | Show that any two cards share exactly one symbol. Groups build decks with 2 symbols per card (3 cards) and 3 per card (aim for 7 cards). |
| 0:10–0:30 | Axioms and the Fano plane | State the axioms, reveal the 7-card deck as the Fano plane, groups prove the counting theorem with the hints below. |
| 0:30–0:55 | Coordinates over F\_q | Points and lines as triples up to scaling, incidence by dot product, joining by cross product. Label the Fano plane with binary triples. |
| 0:55–1:05 | Break |  |
| 1:05–1:45 | Problem session | Problems 1–5 in groups. |
| 1:45–2:00 | Presentations and teaser | Groups present. Pose the open question (which orders exist?) and hand out homework. |

### Board notes: axioms and counting

A projective plane is a set of points and lines such that:

1. Any two distinct points lie on exactly one line.
2. Any two distinct lines meet in exactly one point.
3. There are four points with no three on a line.

**Theorem.** A finite projective plane has an order n ≥ 2: every line has n + 1 points, every point lies on n + 1 lines, and there are n² + n + 1 points and n² + n + 1 lines.

Hints to give groups one at a time:

- If point P is not on line ℓ, the lines through P match up one-to-one with the points of ℓ.
- For any two lines, there is a point on neither (this is where axiom 3 is used), so all lines have the same size.
- Fix a point P. Every other point lies on exactly one line through P, which gives 1 + (n + 1)n points.

### Board notes: the plane over F\_q

- **Points:** nonzero triples (x, y, z) over F\_q, where a triple and its nonzero multiples count as the same point.
- **Lines:** nonzero triples \[a, b, c\], also up to scaling.
- **Incidence:** point (x, y, z) is on line \[a, b, c\] when ax + by + cz = 0.
- **Joining:** the line through points p and r is p × r, and two lines meet at the cross product of their triples. This works over any field, since p × r is orthogonal to both and is nonzero exactly when p and r are not multiples.

```latex
(x_1,y_1,z_1)\times(x_2,y_2,z_2) = (y_1z_2-z_1y_2,\; z_1x_2-x_1z_2,\; x_1y_2-y_1x_2)
```

Counting points: q³ − 1 nonzero triples, grouped q − 1 at a time, gives the plane of order q.

```latex
\frac{q^3-1}{q-1} = q^2+q+1
```

**Over F₂** the points are the 7 nonzero binary triples, and three points are collinear exactly when they XOR to 000. Students who know Nim enjoy this. Have them label a printed Fano diagram, e.g. the line x = 0 holds 010, 001, 011.

**Spot It fact:** the commercial deck is built on the plane of order 7 (57 symbols, 8 per card), though the boxed deck includes only 55 of the 57 possible cards.

## Lecture 1 problem set

Five problems for the 40-minute session; most groups should finish 1–3, strong groups reach 4 and 5.

**Problem 1 (★) Committees.** A club has 7 members. Every committee has exactly 3 members, and every two members serve together on exactly one committee.

- (a) How many committees are there, and how many is each member on?
- (b) Show that any two committees share exactly one member.

**Problem 2 (★) Coordinates.** In the projective plane over F₃, find the line through the points (1, 1, 0) and (0, 1, 2). List all of its points and check there are 4. How many points does the whole plane have?

**Problem 3 (★★) Spot It.** Each card in a deck shows k symbols, and any two cards share exactly one symbol.

- (a) Show the deck can have infinitely many cards.
- (b) Show that if no symbol appears on every card, there are at most k² − k + 1 cards.
- (c) For k = 3, give a deck that reaches this bound.

**Problem 4 (★★) Rectangle-free grid.** Some cells of a 7 × 7 grid are colored so that no four colored cells are the corners of a rectangle with sides along the grid lines. What is the largest possible number of colored cells?

**Problem 5 (★★★) Arcs.** In a projective plane of order n, let S be a set of points with no three on a line.

- (a) Show that S has at most n + 2 points.
- (b) Show that if n is odd, S has at most n + 1 points.

## Homework between lectures

Four problems that bridge to Lecture 2; H1 and H2 come back as the setup for the polarity graph, and H4 previews Latin squares.

**H1 (★★) Graphs without 4-cycles.** A graph has n vertices and no cycle of length 4. Show its number of edges is at most the bound below. Hint: count paths of length 2 through each vertex.

```latex
e \le \frac{n}{4}\left(1+\sqrt{4n-3}\right)
```

**H2 (★★) Bigger grids.** Generalize Problem 4: in an N × N grid with N = q² + q + 1, a rectangle-free coloring has at most (q + 1)(q² + q + 1) cells. Use the plane over F₃ to color 52 cells of a 13 × 13 grid.

**H3 (★★★) Sylvester–Gallai.** Prove that for any finite set of points in the ordinary plane, not all on one line, some line passes through exactly two of them. Deduce that the Fano plane cannot be drawn with straight lines. Hint: among all pairs of a point and a line through two other points of the set, take the pair at the smallest positive distance.

**H4 (★) Latin squares.** A Latin square of order n is an n × n grid filled with 1, …, n so each row and column contains each number once. Two Latin squares are orthogonal if, when overlaid, every ordered pair of entries appears exactly once. Find two orthogonal Latin squares of order 3, and try order 2.

## Lecture 2: Linear algebra as a combinatorial weapon

Subsets become vectors over F₂, and dimension arguments give clean bounds; the lecture closes by showing projective planes nearly meet the H1 bound and telling the story of which orders exist.

| Time | Segment | What happens |
| --- | --- | --- |
| 0:00–0:15 | Homework review | Students present H1 and H3. |
| 0:15–0:35 | F₂ as a language for subsets | The dictionary and three key facts below. |
| 0:35–0:55 | Oddtown and Eventown | Groups attempt Problems 1–2, then one group presents. |
| 0:55–1:05 | Break |  |
| 1:05–1:30 | Lights Out | Play the 3 × 3 game by hand, then a guided proof of Problem 3(b). |
| 1:30–1:45 | Planes as extremal objects | The polarity graph (Problem 4) nearly meets the H1 bound. |
| 1:45–2:00 | Which orders exist? | The existence story below, plus a preview of real projective geometry. |

### Board notes: the F₂ dictionary

| Sets | Vectors over F₂ |
| --- | --- |
| Subset A of {1, …, n} | 0/1 vector of length n |
| Symmetric difference | Sum |
| Parity of the intersection size of A and B | Dot product A · B |
| Parity of the size of A | A · A |

Three key facts:

1. More than n vectors in F₂ⁿ are linearly dependent.
2. If v₁, …, vₘ satisfy vᵢ · vᵢ = 1 and vᵢ · vⱼ = 0 for i ≠ j, they are independent (dot a dependency with each vᵢ).
3. For a subspace W, dim W + dim W⊥ = n. This still holds over F₂, even though W and W⊥ can overlap.

### Board notes: the polarity graph

Vertices are the points of the plane over F\_q, and x is joined to y (x ≠ y) when x · y = 0. A common neighbor z of x and y must satisfy z · x = z · y = 0, so z is the single point x × y. Two vertices have at most one common neighbor, so there is no 4-cycle.

Comparing with H1 for n = q² + q + 1 (where 4n − 3 = (2q + 1)²), the construction falls short of the bound by only (q + 1)/2 edges:

```latex
\text{polarity graph: } \frac{q(q+1)^2}{2} \qquad \text{H1 bound: } \frac{(q+1)(q^2+q+1)}{2}
```

### Board notes: which orders exist?

- A projective plane of order n exists exactly when there are n − 1 mutually orthogonal Latin squares of order n.
- Every prime power q works: the squares L\_a(i, j) = a·i + j over F\_q, for each nonzero a, are mutually orthogonal.
- Order 6 fails. This is Euler's 36 officers problem, settled by Tarry around 1900.
- The Bruck–Ryser theorem (1949): if n ≡ 1 or 2 (mod 4) and n is not a sum of two squares, there is no plane of order n. This rules out 6, 14, 21, 22, and infinitely many more.
- Order 10 passes Bruck–Ryser (10 = 9 + 1) but was ruled out by a massive computer search in 1989.
- Order 12 is open. No one knows if any non-prime-power order exists.

## Lecture 2 problem set

Problems 1 and 3(a) are for everyone; 3(b) is the centerpiece and works best as a guided proof at the board.

**Problem 1 (★) Oddtown.** A town has n residents. Every club has an odd number of members, and every two clubs share an even number of members. Show there are at most n clubs.

**Problem 2 (★★) Eventown.** Now every club has an even number of members, every two clubs share an even number, and no two clubs have the same members.

- (a) Construct 2^⌊n/2⌋ clubs.
- (b) (★★★) Show there can be no more.

**Problem 3 Lights Out.** Pressing a light toggles it and its neighbors.

- (a) (★) On a 3 × 3 board where neighbors share a side, start with all lights on and turn them all off.
- (b) (★★★) Prove that on any finite graph, where pressing a vertex toggles it and all its neighbors, you can get from all lights on to all lights off.

**Problem 4 (★★) The polarity graph.** Using the polarity graph from the board notes:

- (a) Prove it has no 4-cycle.
- (b) Given that exactly q + 1 points satisfy x · x = 0, show it has q(q + 1)²/2 edges.
- (c) Draw it for q = 2 and check you get 9 edges.

**Problem 5 (★★★) Fisher's inequality.** A town has n residents and m distinct clubs, and every two clubs share exactly λ members, where λ ≥ 1. Show that m ≤ n. Hint: work over the real numbers and show the clubs' 0/1 vectors are independent.

## Solutions and teaching notes

Sketches only, at the level you would write on the board; students should be asked to write full versions.

### Lecture 1

**Problem 1.** (a) There are 21 pairs and each committee covers 3, so 7 committees. Each member has 6 partners and each committee covers 2 of them, so each member is on 3 committees. (b) Two committees share at most one member, or a pair would be covered twice. Fix committee C: each of its 3 members is on 2 other committees, giving 6 committees that meet C. These are distinct, so they are all 6 other committees.

**Problem 2.** (1, 1, 0) × (0, 1, 2) = (2, −2, 1) = (2, 1, 1) mod 3, so the line is 2x + y + z = 0. Its points are (1, 0, 1), (1, 1, 0), (1, 2, 2) and (0, 1, 2). The whole plane has 13 points.

**Problem 3.** (a) Put one symbol x on every card and give each card k − 1 symbols of its own. (b) Suppose x is on at least k + 1 cards. Removing x, those cards are pairwise disjoint, so a card without x would need k + 1 different symbols to meet each of them. Hence every card contains x. So if no symbol is on every card, each symbol is on at most k cards. Fix a card C: every other card meets C in exactly one symbol, and each of C's k symbols is on at most k − 1 other cards, giving at most 1 + k(k − 1). (c) The Fano plane: 123, 145, 167, 246, 257, 347, 356.

Teaching note: part (a) is the trap. Many students will "prove" a bound without the extra condition, which makes a good discussion about checking hypotheses.

**Problem 4.** The answer is 21. Let rᵢ be the number of colored cells in row i. Two columns can both be colored in at most one row, so the sum of C(rᵢ, 2) is at most C(7, 2) = 21. With 22 cells, the most even split is six rows of 3 and one of 4, giving 6 · 3 + 6 = 24 > 21. For 21, let rows be the lines and columns the points of the Fano plane, coloring a cell when the point is on the line. A rectangle would mean two lines sharing two points.

**Problem 5.** (a) Fix P in S. The other points of S lie on different lines through P, and there are n + 1 such lines, so S has at most n + 2 points. (b) If S has n + 2 points, every line through any P in S meets S exactly once more, so every line meets S in 0 or 2 points. Take a point Q outside S: the n + 1 lines through Q split S into pairs, so n + 2 is even, and so is n.

### Homework

**H1.** Two vertices have at most one common neighbor, so the sum over vertices of C(d(v), 2) is at most C(n, 2). By convexity, with average degree d = 2e/n, this gives d(d − 1) ≤ n − 1, so d ≤ (1 + √(4n − 3))/2, and e = nd/2.

**H2.** The same count as Problem 4 shows the average row has at most q + 1 cells. For 13 × 13, use the 13 lines and 13 points of the plane over F₃, with 4 points per line, giving 52 cells.

**H3.** Take P and a line ℓ through two points of the set, with P off ℓ at the smallest positive distance. If ℓ held three points, two of them, A and B, would lie on the same side of the foot F of the perpendicular from P, with B between F and A (or at F). Then B is closer to line PA than P is to ℓ, a contradiction. In the Fano plane every line through two points has a third, so it cannot be drawn.

**H4.** Order 3: use L₁(i, j) = i + j and L₂(i, j) = i + 2j mod 3. Order 2 has no orthogonal pair, which is not a contradiction: a plane of order 2 only needs n − 1 = 1 Latin square.

### Lecture 2

**Problem 1.** The club vectors satisfy v · v = 1 and vᵢ · vⱼ = 0 over F₂, so they are independent by key fact 2, and there are at most n.

**Problem 2.** (a) Pair up the residents and take every union of pairs. (b) The vectors are pairwise and self-orthogonal, so their span W lies inside W⊥. Key fact 3 gives 2 dim W ≤ n, so W has at most 2^⌊n/2⌋ vectors.

**Problem 3.** (a) Press the four corners and the center: each corner and the center toggle once, each edge cell three times. (b) Let M = A + I over F₂, with A the adjacency matrix. You need the all-ones vector **1** in the column space of M, which equals (ker M)⊥ since M is symmetric (one inclusion is direct, and dimensions match by key fact 3). For x in ker M, expand xᵀMx. Off-diagonal terms come in equal pairs and cancel, the diagonal is all 1s, and xᵢ² = xᵢ, so:

```latex
0 = x^{T}Mx = \sum_i x_i = \mathbf{1}\cdot x
```

So **1** is orthogonal to ker M, hence a solution z of Mz = **1** exists, and pressing the vertices where z is 1 does the job.

**Problem 4.** (a) A 4-cycle would give two opposite vertices two common neighbors. (b) Each x has q + 1 points z with x · z = 0 (a whole line), but when x · x = 0, x is one of them, so its degree is q. Degrees sum to (q + 1)(q² + q + 1) − (q + 1) = (q + 1)(q² + q). (c) For q = 2, the points 110, 101, 011 have degree 2 and the other four have degree 3, giving 18/2 = 9 edges.

**Problem 5.** Every club has at least λ members, and at most one has exactly λ (such a club lies inside every other, so two of them would be equal). If a combination of the club vectors is zero, expand its squared length:

```latex
0 = \Big|\sum_i c_i v_i\Big|^2 = \lambda\Big(\sum_i c_i\Big)^2 + \sum_i c_i^2\big(|C_i|-\lambda\big)
```

Every term is nonnegative, so cᵢ = 0 for every club larger than λ, and then the sum being 0 forces the last coefficient to 0. The vectors are independent, so m ≤ n.
