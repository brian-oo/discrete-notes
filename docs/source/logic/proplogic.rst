
********************
Propositional Logic
********************

.. contents:: Table of Contents
    :local:

------------
Propositions
------------

In order to begin our journey in any proof-based math class, we must start with the building block: propositions. If logic and proofs were a house, propositions are the bricks. A **proposition** is a declarative statement that is either *true* or *false*. Propositions must be true or false, and can not be neither true nor false, nor be both true and false. Propositions are strictly binary and must maintain only one truth value at a time.


.. container:: toggle

    .. container:: header

        **▶ EECS Extension**

    .. compound:: 

       Requiring propositions be either true or false, not neither or both, is more than a math principle. Propositions in the coding world can be considered as ``boolean`` where at any given point your ``boolean`` is true/false, but never nothing nor both. This extends even further, down to the hardware. On a circuitry level, wires and transistors can either be on or off. This is determined through voltage levels. Most transistors have a threshold voltage, such that once a particular wire reaches a threshold voltage, the transistor turns on. Gather thousands of silicon transistors together, and you just made a microprocessor.


The other major component of a proposition is that it be a declarative statement. Exclamatory statements, such as "Wow!" have no truth value, nor do questions, such as "Is it raining?" It may seem natural to think the answer to the question represents the truth value, however the question itself does not have a truth value. The statement "It is raining right now" does maintain an active truth value, and is therefore a proposition.  

Note that we do not have to know the truth value of a proposition to consider it a proposition. "Aliens exist" is a proposition, however we do not know its truth value. Nonetheless we can still use propositional logic on this proposition, despite not knowing its exact truth value. **Axioms** are propositions, that we assume to be true and are assumed to be true at all times, such as :math:`1 + 1 = 2`. 


----

**Sample Problem**

Which of the following are propositions: 

1. A square has 4 sides.
2. All rectangles are squares.
3. Is a rectangle a square?
4. This statement is false.
5. :math:`8 \cdot 2 = 16`
6. :math:`8 \cdot x = 16`


.. container:: toggle

    .. container:: header

        **▶ Solution**

    .. container:: blank

        1. Proposition, its truth value is true.  
        2. Proposition, its truth value is false.
        3. Not a Proposition, questions do not have a truth value.
        4. Not a Proposition, paradoxes do not have a definite truth value.
        5. Proposition, its truth value is true.
        6. Not a Proposition. This is a predicate.


----

Number 6 is tricky. :math:`8 \cdot x = 16` is a proposition only if we have a value for :math:`x`. At the moment, the statement is a predicate because we are unsure what :math:`x` is. If :math:`x` was a sandwich, then the proposition :math:`8 \cdot x = 16` makes no sense. Only once we define posible values (domain) for :math:`x` then we can claim there is a truth value. "Given that :math:`x` is a real number, :math:`8 \cdot x = 16`" is a proposition since although we do not know if the value of :math:`x` , we know that the statement is either true or false, thus making it a proposition. 

---------------------
Compound Propositions
---------------------

In order to simplify logical expressions, we can use letters: such as :math:`p, q, r` to represent propositions. Let's say we have propositions: :math:`p =` "*It rained today*" and :math:`q =` "*I brought my umbrella today*". How could we express the logical statement: "*It rained today and I brought my umbrella.*" We could define a new proposition, :math:`r` to represent this statement, however this will get tedious the more and more expressions we have. The way to combine propositions is with logical operators.

=================
Logical Operators
=================

If we want to express both the logical expression of both :math:`p` and :math:`q`, we use the *and* operator: :math:`\wedge`. Therefore, to represent the statement "*It rained today and I brought my umbrella*": :math:`p \wedge q`. A table of logical operators is below: 

[INSERT TABLE BELOW]

.. admonition:: Or vs. Xor

    In logic we have two ways to express the English word "*or*". This is because there are some instances where we need an inclusive-or or an exclusive-or (xor). For example, the or in "*Today or tomorrow is her birthday*" is an exclusive-or since both situations can not both be true. Meanwhile the or in "*Would you like cream or sugar*" is inclusive because wanting cream, sugar, or both would all be valid responses.

.. tip:: 
    Implication is naturally unintuitive. Saying that if :math:`p` then :math:`q` suggests that there is a causal relationship between :math:`p` and :math:`q`, however we must obey the truth table. The proposition ":math:`(0 = 1) \rightarrow` *pigs can fly*" is true. This is because :math:`(0 = 1)` is false and "*pigs can fly*" is false, and according to the truth table  :math:`F \rightarrow F = T`. It takes practice to intuitively understand how implications work. 

    * If :math:`p` is true, then the truth value of :math:`p \rightarrow q`depends on :math:`q`.
    * If :math:`p` is false, then the truth value of :math:`p \rightarrow q` is true, no matter what :math:`q` is.
    * It may help to look from the false perspective: :math:`p \rightarrow q` is false **only** if :math:`p` is true and :math:`q` is false.


