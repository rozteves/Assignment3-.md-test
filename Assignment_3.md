# Assignment3-.md-test

Part 1:

S = it is sunny, C = camping is fun, H = the homework is done, M = mathematics is easy

Translate - (M->H)^(S->C)
"If mathematics is easy then the homework is done, and if it is sunny then camping is fun.

Translate - "Mathematics is easy or camping is fun, as long as it is sunny and the homework is done"
(MvC)->(S^H)

-----------------------------------------------------------------------------------------------------------

Part 2:

(¬B → ¬A) → ((¬B → A) → B)

A|B|¬A|¬B|(¬B → ¬A)|(¬B → A)|((¬B → A) → B)|(¬B → ¬A) → ((¬B → A) → B)|
-----------------------------------------------------------------------
T|T|F |F |T        |T       |T             |T                         |
T|F|F |T |F        |T       |F             |T                         |
F|T|T |F |T        |T       |T             |T                         |
F|F|T |T |T        |F       |T             |T                         |

Equation is a tautology.


((A → B)∧(B → ¬A)) → A

A|B|¬A|¬B|(A → B)|(B → ¬A)|((A → B)∧(B → ¬A))|((A → B)∧(B → ¬A)) → A|
---------------------------------------------------------------------
T|T|F |F |T      |F       |F                 |T                     |
T|F|F |T |F      |T       |F                 |T                     |
F|T|T |F |T      |T       |T                 |F                     |
F|F|T |T |T      |T       |T                 |F                     |

Equation is neither.

-----------------------------------------------------------------------------------------------------------

Part 3:

(p ∧ q) → r , p → (q → r )

(p ∧ q) → r <=> p → (q → r )
            <=> p' v (q' v r)		  Implication 
            <=> (p' v q') v r		  Associative
            <=> (p ^ q)' v r		  De Morgan's Laws
            <=> ((p ^ q)')' -> r	Implication
	          <=> (p ^ q) -> r		  Double Negation
(p ∧ q) → r <=> (p ∧ q) → r


(q ∨ r ) → p, (q → p)∧(r → p)

(q v r) -> p <=> (q -> p)^(r -> p)
	           <=> (q' v p)^(r' v p) Implication
	           <=> p v (q' ^ r')		 Distributive
	           <=> (q' ^ r') v p		 Communative
	           <=> (q v r)' v p	     De Morgan's Laws 
	           <=> ((q v r)')' -> p	 Implication
	           <=> (q v r) -> p		   Double Negative
(q v r) -> p <=> (q v r) -> p

-----------------------------------------------------------------------------------------------------------

Part 4:

Loves(x,y) = "x loves y," Traveler(x) = "x is a traveler,"
City(x) = "x is a city," Lives(x,y) = "x lives in y."

Translate into English: ∃x∀y∀z(City(x) ∧ Traveler(y) ∧ Lives(z,x)) → (Loves(y,x)∧ ¬Loves(z,x))
"If there are some cities, all travelers, and all residents, then all travelers love all cities and all residents do
not love all cities."

Translate into Predicate Logic: “No traveler loves the city they live in.”
∀x∀y ((Traveler(x) ^ City(y) ^ Lives(x,y)) -> ¬Loves(x,y))

-----------------------------------------------------------------------------------------------------------
Extra Credit:

Assuming: p → (q ∧ r ), s → r , r → p
Prove: s → q.

1. s		assumption
2. p -> (q ^ r) premise 
3. s -> r	premise
4. r -> p	premise
5. q ^ r 	Modus Ponens
6. r 		Modus Ponens
7. p		Modus Ponens
8. s -> q	Steps 2-7


Assuming: ¬(r ∨ s), ¬p → s, p → q. 
Prove: q 

1. ¬(r v s)	assumption
2. ¬r ^ ¬s	De Morgan's
3. ¬s		2
4. ¬p -> s	Premise
5. p -> ¬s	Modus Tollens
6. p		5
7. p -> q	Premise
8. q		Modus Ponens

