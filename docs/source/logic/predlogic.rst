
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

A relation can have just a single argument; we can call this a property of the objects. For example, let :math:`P(x)` be ":math:`x` *will buy an apple*". The statement, "*If you buy an apple, then I'll buy an apple*" can be represented as :math:`P(\text{You}) \rightarrow P(\text{Me})`. 

How can we represent the phrase "*Everyone will buy an apple*"? We run into the issue where there may be an infinite number of things to account for or we do not know everyone in the list. Nonetheless, we need to represent the fact that everyone will buy an apple. 

To do so, we can use quantifiers. Applying a quantifier to a predicate, creates a proposition.

Universal Quantifier
^^^^^^^^^^^^^^^^^^^^

The universal quantifier, represented by the symbol :math:`\forall`, spoken as "*for all*" represents every element. :math:`\forall x P(x)` represents "*Everyone will buy an apple*". This can be conceptualized as :math:`P(x_1) \wedge P(x_2) \wedge P(x_3) \wedge ...` , since for every element :math:`x_n`, they must buy an apple. 

Whenever we say for all :math:`x`, we must define the **domain of discourse** (also called the universe of discourse). `Wikipedia <https://en.wikipedia.org/wiki/Domain_of_discourse>`_ defines the domain of discourse as

    *the set of entities over which certain variables of interest in some formal treatment may range. In first-order logic, the domain of discourse is the set of individuals over which the quantifiers range.*

Without defining the domain of discourse, predicates are ambigious. In :math:`\forall x P(x)`, :math:`x` itself be anything, however by specifying the domain of discourse, we can specify our domain as all people, all people in a class, all pets of people in a class, anything.

Existential Quantifier
^^^^^^^^^^^^^^^^^^^^^^

The existential quantifier, represented by the symbol :math`\exists`, spoken as "*there exists*" represents some element. In other words, it means at least one element has this property. Again, we must specify to domain of discourse to know what pool of elements we are choosing from.

Under the existential quantifier, anywhere from one to every element in the domain of discourse has the property. The existential quantifier can be conceptualized as :math:`P(x_1) \vee P(x_2) \vee P(x_3) \vee ...`, since anywhere from one to all of the elements :math:`x_n` would cause the statement to be true.

------------------
Nested Quantifiers
------------------

When using multiple instances of an element or multiple different quantifiers, we must be careful with the scope and ordering of these elements, as different propositions can have different meanins when order is changed.

Scope of Quantifiers
^^^^^^^^^^^^^^^^^^^^

Let :math:`B(x,y)` mean :math:`x` buys :math:`y`. 

"*Everyone will buy an apple or a pear.*" For this sentence, every person has the option to buy either an apple or a pear, however all people must buy at least one. Everyone does not have to buy the same item. This is represented as:

:math:`\forall x \underline{(B(x, \text{Apple}) \vee B(x, \text{Pear} ) )}`


In this example, there is only one quantified variable, :math:`x` and the scope of this variable is the entire underlined statement.

"*Everyone will buy an apple or everyone will buy a pear*." For this sentence every person must buy the same item, and that item is either an apple or a pear. For either item, the entire population must have the same item, or else the statement is false. This is represented as: 

:math:`\forall x \underline{B(x, \text{Apple})} \vee \forall x \underline{B(x, \text{Pear} ) }`


In this example there are two quantified variable, and for each variable, there is a unique scope for the variable. This has to potential to cause confusion, so we try to avoid it by having two unique variables representing the two different quantifications. :math:`\forall x \underline{B(x, \text{Apple})} \vee \forall y \underline{B(y, \text{Pear} ) }`

Order of Quantifiers
^^^^^^^^^^^^^^^^^^^^

When using multiple variables and quantifiers, the understanding the order is essential to understanding the statement. Quantifiers are processed in the order they are read, meaning that the first quantifier is applied, and every other quantifier after is contained within the scope of the first quantifier:

Let the domain of :math:`x` be people and let the domain of :math:`y` be items in a shop 

:math:`\forall x \exists y B(x,y)` means for every person, they must buy some item. It does not have to be the same item for everyone, but for each person they must buy some item.

* The :math:`\forall x` scope is created first, meaning for all people, we must handle some proposition
* Then a :math:`\exists y` scope is create for each person. These :math:`y` do not have to be the same for every person.
* This can be thought as :math:`\exists y B(x_1, y) \wedge \exists y B(x_2, y) \wedge \exists y B(x_3, y) \wedge ...`
* Since each instance of :math:`\exists y` is seperate, we can treat this as :math:`\exists y B(x_1, a) \wedge \exists y B(x_2, b) \wedge \exists y B(x_3, c) \wedge ...` where :math:`a,b,c` are in the same domain as :math:`y`.
* Practically, this just means that every customer :math:`x_1, x_2, x_3, ...` must buy some item :math:`a, b, c,...` however these items do not have to be related, other than all being items from the shop. 
* It is possible that all items can be the same, however is not required in order for the proposition to be true.

----

**Sample Problem**

Using the same predicates and domains as before, translate the following statements into English.

1. :math:`\forall x \forall y B(x,y)`.
2. :math:`\exists x \exists y B(x,y)`.
3. :math:`\forall y \exists x B(x,y)`.
4. :math:`\exists x \forall y B(x,y)`.
5. :math:`\exists y \forall x B(x,y)`.

.. container:: toggle

    .. container:: header

        **▶ Solution**

    .. container:: blank

        1. Every person bought every item in the shop.
        2. There exists a person who bought some item in the shop.
        3. For every item in the shop, there exists someone who bought it.
        4. There exists a person who bought every item in the shop.
        5. There exists some item that everyone in the shop bought.

----

--------------------
Negating Quantifiers
--------------------

In order to negate a quantifier, we change the quantifier type and then negate the predicate.

.. math::

    \neg \forall x P(x) \equiv \exists x \neg P(x) \\
    \neg \exists x P(x) \equiv \forall x \neg P(x)

.. Note::
    This property comes from De Morgan's law. Recall that according to De Morgan's law, when negating an and or or, we apply the negation to the propositions and switch the logical operator. Also recall that universal and existential quantifiers are really an extended series of ands and ors respectively. 

When negating nested quantifiers, each quantifer gets negated one at a time and any other quantifiers get treated as the interior predicate that gets negated.

----

**Sample Problem**

Simplify the following statement: :math:`\neg \forall a \exists b \forall c P(a, b, c)`

.. container:: toggle

    .. container:: header

        **▶ Solution**

    .. container:: blank

        .. math:: 
            \begin{aligned}
                &\neg \forall a \exists b \forall c P(a, b, c) \\
                & \equiv \exists a \neg ( \exists b \forall c P(a,b,c)) \\
                & \equiv \exists a \forall b \neg (\forall c P(a,b,c)) \\
                & \equiv \exists a \forall b \exists c \neg P(a,b,c)
            \end{aligned}

----

----------------------
Translating Predicates
----------------------





