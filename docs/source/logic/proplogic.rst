
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

    .. container:: blank

       Requiring propositions be either true or false, not neither or both, is more than a math principle. Propositions in the coding world can be considered as ``boolean`` where at any given point your ``boolean`` is true/false, but never nothing nor both. This extends even further, down to the hardware. On a circuitry level, wires and transistors can either be on or off. This is determined through voltage levels. Most transistors have a threshold voltage, such that once a particular wire reaches a threshold voltage, the transistor turns on. Gather thousands of silicon transistors together, and you just made a microprocessor.



The other major component of a proposition is that it be a declarative statement. Exclamatory statements, such as "Wow!" have no truth value, nor do questions, such as "Is it raining?" It may seem natural to think the answer to the question represents the truth value, however the question itself does not have a truth value. The statement "It is raining right now" does maintain an active truth value, and is therefore a proposition.  

Note that we do not have to know the truth value of a proposition to consider it a proposition. "Aliens exist" is a proposition, however we do not know its truth value. Nonetheless we can still use propositional logic on this proposition, despite not knowing its exact truth value. **Axioms** are propositions, that we assume to be true and are assumed to be true at all times, such as :math:`1 + 1 = 2`. 


----

Sample Problem
^^^^^^^^^^^^^^

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

Number 6 is tricky. 

