
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

An example of a set is :math:`\{2, 3, 6\}`. Items in a set are called elements. For example, :math:`2` is an element in the set :math:`\{2, 3, 6\}`. We notate this as :math:`2 \in \{2, 3, 6\}` There are several key properties to the definition of a set:

* A set is made up of distinct objects. :math:`\{2, 3, 6, 6\}` is the same set as :math:`\{2, 3, 6\}`. :math:`6` is in the set only once, despite being written twice. There is no count for any elements in a set, the only property that matters for an element is whether it is in the set or not.
* A set is unordered. :math:`\{2, 3, 6\}` is the same set as :math:`\{3, 6, 2\}` since the order of a set does not matter. Sets can be thought of as a collective group of objects, without one having precedent over another. 
* A set is considered an object, meaning a set can be an element of another set.

Sets can contain anywhere from an infinite amount of elements to no elements. A set with no elements is called the **empty set** :math:`\emptyset`.

Set Builder Notation
^^^^^^^^^^^^^^^^^^^^

When sets have a small, finite amount of elements it is easy to list all the items; however, when sets have a large or even infinite amount of elements this task becomes impossible. To alleviate this, we use a membership predicate: a :doc:`predicate <../logic/predlogic>` that defines whether or not a particular element is in the set. 

.. math:: 
    A = \{ x | P(x) \}

* :math:`A`: the set being defined
* :math:`x`: all of the elements in the domain.
* :math:`|`: "such that"
* :math:`P(x)`: the membership predicate. If the predicate is true for a given input element, the element is in the set.

