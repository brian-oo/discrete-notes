
****
Sets
****

.. contents:: Table of Contents
    :local:

----------------
Set Fundamentals
----------------

One of the fundamentals of discrete math is the study of discrete structures. Graphs, trees, functions and more all rely on sets. These discrete structures are integral to modern computer science and form the data structures that make up modern computing.

`Wikipedia <https://en.wikipedia.org/wiki/Set_(mathematics)>`_ defines a mathematical set as

    *a well-defined collection of distinct objects, considered as an object in its own right. The arrangement of the objects in the set does not matter...The concept of a set is one of the most fundamental in mathematics. Developed at the end of the 19th century, set theory is now a ubiquitous part of mathematics, and can be used as a foundation from which nearly all of mathematics can be derived.*

An example of a set is :math:`\{2, 3, 6\}`. Items in a set are called elements. For example, :math:`2` is an element in the set :math:`\{2, 3, 6\}`. We notate this as :math:`2 \in \{2, 3, 6\}`. There are several key properties to the definition of a set:

* A set is made up of distinct objects. :math:`\{2, 3, 6, 6\}` is the same set as :math:`\{2, 3, 6\}`. :math:`6` is in the set only once, despite being written twice. There is no count for any elements in a set, the only property that matters for an element is whether it is in the set or not.
* A set is unordered. :math:`\{2, 3, 6\}` is the same set as :math:`\{3, 6, 2\}` since the order of a set does not matter. Sets can be thought of as a collective group of objects, without one having precedent over another. 
* A set is considered an object, meaning a set can be an element of another set.

Sets can contain anywhere from an infinite amount of elements to no elements. A set with no elements is called the **empty set** :math:`\emptyset`. A set containing all of the elements in the domain is called the **universal set** :math:`U`.

Set Builder Notation
^^^^^^^^^^^^^^^^^^^^

When sets have a small, finite amount of elements it is easy to list all the items; however, when sets have a large or even infinite amount of elements this task becomes impossible. To alleviate this, we use a membership predicate: a :doc:`predicate <../logic/predlogic>` that defines whether or not a particular element is in the set. 

.. math:: 
    A = \{ x | P(x) \}

* :math:`A`: the set being defined
* :math:`x`: all of the elements in the domain of discourse.
* :math:`|`: "such that"
* :math:`P(x)`: the membership predicate. If the predicate is true for a given input element, the element is in the set.

--------------
Set Operations
--------------

Just like with propositions, sometimes we need to describe some combination of multiple sets. To do so, we can use set operations.

The set **union** of two sets consists of all of the elements that are in either of the sets or both. The set **intersection** of two sets consists of all the elements that are strictly in both sets. The set **complement** of a set is all of the elements within the domain that are not in the given set. The set **minus** operation represents all of the elements that are in the first set but are not in the second set. 

Let the domain be the integers between 1 and 10 inclusive. :math:`A = \{ 2, 3, 6 \}`. :math:`B = \{ 1, 3, 5, 6 \}`.

.. table:: Table of Set Operations
    :widths: auto
    :align: center

    ============    =====================   ==============================         
    Name            Set Operation           Resulting Set
    ============    =====================   ==============================
    Union           :math:`A \cup B`        :math:`\{1, 2, 3, 5, 6,\}`
    Intersection    :math:`A \cap B`        :math:`\{3, 6\}`
    Complement      :math:`\overline{B}`    :math:`\{2, 4, 7, 8, 9, 10 \}`
    Minus           :math:`A - B`           :math:`\{2\}`
    ============    =====================   ==============================


-------
Subsets
-------

Alongside being able to combine sets using set operations, we can also describe the relationship between multiple sets. The most important relation between two sets is the subset relation. 

The mathematical definition of a **subset** is :math:`\forall x (x \in S \rightarrow x \in T)` where :math:`S` is a subset of :math:`T`. Practically, in order for set :math:`S` to be a subset of set :math:`T`, then every element in :math:`S` must be in :math:`T`. 

For example, the set of all oranges is a subset of the set of all fruits because every orange in the set of all oranges is also in the set of all fruits. This relation is not symmetrical, as there are some elements in the set of all fruits (like apples) that are not in the set of all oranges. We notate this relation as :math:`S \subseteq T`.

If a set is subset of another set, *and those sets are not the same set*, then we call this a **proper subset**. We notate this as :math:`S \subset T`.

Two sets are **disjoint** if and only if they do not share any elements. In other words, if we had two sets :math:`A` and :math:`B`, and their intersection :math:`A \cap B` was the empty set :math:`\emptyset`, then they are disjoint.

Power Sets
^^^^^^^^^^

The **power set** of a set is a set that contains every possible subset of the original set. For example, let :math:`A = \{ 1, 2, 3 \}`. The power set of :math:`A`, 

.. math::
    P(A) = \{ \emptyset, \{ 1 \}, \{ 2 \}, \{ 3 \}, \{1, 2\}, \{1, 3\},\{2, 3\}, \{1, 2, 3\} \}

If a given set has :math:`n` elements in it, the power set will consist of :math:`2^n` different sets.

The empty set will always be in a power set because the empty set is a subset of every possible set (including the empty set). This is because in the mathematical definition :math:`\forall x (x \in S \rightarrow x \in T)`, the left hand side of the implies statement will always be false, since there are no elements in the empty set. Another way of conceptualizing this is if a set is *not* a subset, then there should be an element you can find that is not in the larger set. With the empty set, there are no elements, so there is no way to find this outliar element. 

.. tip::
    When writing out power sets, write them in order of their size. Start with the empty set, then write every subset with one element, every subset with two elements, and so on. This helps keeps things organized and lessens the chance of forgetting a subset. 
    
    Additionally, remember that order does not matter with sets, so having a standard order of writing sets, such as writing elements from least to greatest helps avoid repeating sets that you wrote with different orders.


----------------
Proofs with Sets
----------------

Set Identities
^^^^^^^^^^^^^^

-----------
Cardinality
-----------

Inclusion-Exclusion
^^^^^^^^^^^^^^^^^^^




