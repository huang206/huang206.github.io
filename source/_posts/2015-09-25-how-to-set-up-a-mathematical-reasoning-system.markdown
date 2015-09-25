---
layout: post
title: "How to set up a mathematical reasoning system"
date: 2015-09-25 10:15:40 -0700
comments: true
categories: [math, reasoning]
---
> Explain everything in your own words before you formulate them with logics.

##1.Introduction
Human beings could only understand precise and unambiguous things. Nature languages like English have ambiguity, which could be eliminated by context. However, we need a precise, concise and context-free language to help us abstract the nature. This language is called mathematics. We know that science is built on mathematics. But what is mathematics built on?
The answer is reasoning system, which is created by Euclid. In such a system we could prove new propositions as theorems with axioms and some already proved propositions. These newly proved propositions are accumulated to enlarge our knowledge database. Like rolling a snowball, the mathematics system is set up and constructed layer upon layer.

##2.Terminology
*   **Proposition:**  A statement that is either true or false.
*   **Axioms:** Propositions that has been assumed to be true, considered as foundation in this system.
*   **Theorem:** Important propositions.
*   **Lemma:** A preliminary proposition useful for proving later propositions.
*   **Corollary:** A proposition that follows in just a few logical steps from lemma or a theorem.

>   Ps: Notice that Theorem, Lemma and Corollary have been proved, a proposition has been proved means that we can consider it as true from now on.

*   **Proof:** A sequence of logical deductions from axioms and previously proved propositions that concludes with the proposition in question.
*   **Predicate:** A special proposition whose truth-value depends on its variables.
*   **Quantifiers:** Prefix phrases like “For all n”, “Exist an n” added before a basic predicate which indicates under which values this predicate is true.

>   Ps: Computer program is consisted of statements, which could be assigned a value of true or false. These propositions are useful when you need to do some judgments in the program.

##3.Compound propositions
Notice we could construct compound propositions from the basic ones. This is a way of generative definition.

1.  **Basic step:** Assume P and Q are propositions (We use variables to denote proposition, here we use principles of abstract to get rid of enormous realistic propositions) .
2.  **Generative Step:** Then the following combinations are all propositions.
    *   P AND Q
    *   P OR Q
    *   NOT P
    *   P XOR Q (XOR denotes exclusive-or, which means that you could not have both P and Q to be true at the same time)
    *   P IMPLIES Q (equals to IF P THEN Q)
    *   P IFF Q (indicates that P and Q are logically equivalent)

P and Q could either be true or false, these compound propositions’ truth-value depends on P’s and Q’s truth-value. (So if you want to know whether a compound proposition is true or false, you need to decompose it into basic propositions and ascertain each basic one’s truth-value.)

##4.Predicates and Quantifiers
We usually use function-like notation to denote predicate likes P(n), which means that this proposition P’s truth-value depends on variable n.

>   Ps: predicate notation P(n) is different with function notation P(n), the first one has T or F as return value however the last one has numbers as return value.

Most propositions we will consider in computer science are predicates, the truth-value of these predicates depend on their variables. It’s obvious that different values of these variables lead predicates to different situations.
We have two typical situations:

1.  Always true, for all values of n in domain D, the predicate P(n) is true.
2.  Sometimes true, there exists such n in domain D, the predicate P(n) is true.

We use quantifiers like “For all n”, “Exist an n” to quantify a predicate and the quantified predicates are also propositions.

##5.Validity
A propositional formula is called valid when it evaluates to T no matter what truth-values are assigned to the individual propositional variables.

>   Ex: The Distributive law, [P AND (Q OR R)] IFF [(P AND Q) OR (P AND R)] is true no matter what truth-value of P, R and Q is.

##6.Satisfiability
A proposition formula is satisfiable if some setting of the individual proposition makes the proposition true.

>   Ps: The idea of validity and satisfiability is similar to the idea of always true and sometimes true of Predicates.

##7.Logical Deduction
Logical deduction should obey some rules. A simple rule is consisted of two parts, antecedents and consequents. When the antecedents are proved, we can consider the consequents to be true. The criteria of selecting rules are soundness, which means that any assignment of truth-values that makes all the antecedents true must also make the consequent true.

A fundamental inference rule says that a proof of P with a proof of P IMPLIES Q is a proof of Q.

###How to prove P?
1.  If this is a complicated proof, we can break the proof into cases and prove each case separately.
2.  Prove by contradiction. Assume NOT(P) is true.

###How to prove P IMPLIES Q?
1.  Assume P is true, prove Q is true under condition P is true.
2.  Prove the contrapositive NOT(Q) IMPLIES NOT(P).

###How to Prove P IFF Q?
1.  Prove each statement implies the other.
2.  Construct a chain of IFFs.
