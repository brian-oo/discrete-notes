
***************
Predicate Logic
***************

.. contents:: Table of Contents
    :local:

----------
Predicates
----------

So far we have discussed propositions and logical operators, making compound propositions. Now to further abstract this, we will introduce first-order logic, which utilizes objects, properties, and relations. A **predicate** is a declarative statement with *some terms unspecified*. A predicate *becomes* a proposition when terms are specified. We refer to these terms as *objects*.

Take the proposition "*I am taller than both of my sisters, but they're the same height*." If we were to only use propositional logic, we would need 4 propositions:

* :math:`p =` I am taller than my first sister
* :math:`q =` I am taller than my second sister
* :math:`r =` My first sister is taller than my second sister
* :math:`s =` My second sister is taller than my first sister

We would then translate the original statement as :math:`p \wedge q \wedge \neg r \wedge \neg s`, however this isn't very concice or adaptable to other situations.

.. container:: toggle

    .. container:: header

        **▶ Math Extension**

    .. compound:: 

        Why does :math:`\neg r \wedge \neg s` mean that both sisters are the same height?

        What does :math:`\neg r` mean? Well if the original proposition means "*My first sister is taller than my second sister*", then the negation of it is "*My first sister is shorter than or the same height as my second sister*." We have to remember that the negation of taller than isn't shorter than, but shorter than or equal to. 
        
        Applying this negation to both propositions, we get :math:`\neg r \wedge \neg s` meaning "*My first sister's height is less than or the same as my second sister **and** my second sister's height is less than or the same as my first sister*". The only possible way for this to be true is that their heights are the same since both propositions must be true.

        This is a neat trick we see a lot in mathematics in order to prove two things are equal. Sometimes, it is difficult to directly prove that two things are equal, however easy to prove that one thing is greater-than-or-equal-to another. If we perform this greater-than-or-equal-to proof two times, going in both directions ( :math:`A \geq B` & :math:`B \geq A` ), we can prove that :math:`A = B`. We will see this trick come in again later.
    
We can use predicate logic to explicitly described objects and relations to describe characteristics between objects.

* Objects: :math:`M` = Me, :math:`S_1` = First Sister, :math:`S_2` = Second Sister
* Relation: :math:`T(x,y)` = " :math:`x` *is taller than* :math:`y` ".

Then we can represent the the proposition as :math:`T(M,S_1) \wedge T(M,S_2) \wedge \neg T(S_1, S_2) \wedge \neg T(S_2, S_1)`. When the variables in a relation are bound to objects, the relation becomes a proposition with a true/false value.

--------------
Quantification
--------------

A relation can have just a single argument; we can call this a property of the objects. For example, let :math:`P(x)` be ":math:`x` *will buy an umbrella*". The statement, "*If you buy an umbrella, then I'll buy an umbrella*" can be represented as :math:`P(\text{You}) \rightarrow P(\text{Me})`. 

How can we represent the phrase "*Everyone will buy an umbrella*"? We run into the issue where there may be an infinite number of things to account for or we do not know everyone in the list. Nonetheless, we need to represent the fact that everyone will buy an umbrella. 

To do so, we can use quantifiers. Applying a quantifier to a predicate, creates a proposition.

Universal Quantifier
^^^^^^^^^^^^^^^^^^^^

The universal quantifier, represented by the symbol :math:`\forall`, spoken as "*for all*" represents every element. :math:`\forall x P(x)` represents "*Everyone will buy an umbrella*". This can be conceptualized as :math:`P(x_1) \wedge P(x_2) \wedge P(x_3) \wedge ...` , since for every element :math:`x_n`, they must buy an umbrella. 

Whenever we say for all :math:`x`, we must define the **domain of discourse** (also called the universe of discourse). `Wikipedia <https://en.wikipedia.org/wiki/Domain_of_discourse>`_ defines the domain of discourse as

    *the set of entities over which certain variables of interest in some formal treatment may range. In first-order logic, the domain of discourse is the set of individuals over which the quantifiers range.*

Without defining the domain of discourse, predicates are ambigious. In :math:`\forall x P(x)`, :math:`x` itself be anything, however by specifying the domain of discourse, we can specify our domain as all people, all people in a class, all pets of people in a class, anything.

Existential Quantifier
^^^^^^^^^^^^^^^^^^^^^^

The existential quantifier, represented by the symbol :math`\exists`, spoken as "*there exists*" represents some element. In other words, it means at least one element has this property. Again, we must specify to domain of discourse to know what pool of elements we are choosing from.

Under the existential quantifier, anywhere from one to every element in the domain of discourse has the property. The existential quantifier can be conceptualized as :math:`P(x_1) \vee P(x_2) \vee P(x_3) \vee ...`, since anywhere from one to all of the elements :math:`x_n` would cause the statement to be true.

Nested Quantifiers
^^^^^^^^^^^^^^^^^^

Scope of Quantifiers
""""""""""""""""""""

Order of Quantifiers
""""""""""""""""""""

Negating Quantifiers
^^^^^^^^^^^^^^^^^^^^