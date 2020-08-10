**Proof**: :math:`\overline{A \cup B} = \overline{A} \cap \overline{B}`

**Strategy**: We will use two direct proofs to prove both each set is a subset of the other using an arbitrary element of the set.

**Prerequisite Math**: 
    * Definition of Subset: :math:`x \in A \rightarrow x \in B` 

First we will show that :math:`\overline{A \cup B} \subseteq \overline{A} \cap \overline{B}`. Let :math:`x` be an arbitrary element in :math:`\overline{A \cup B}`. 

.. math::
            \begin{align}
            & x \in \overline{A \cup B} & \text{Given} \\
            & x \notin A \cup B & \text{Def. of Complement} \\
            & \neg [ (x \in A) \vee (x \in B) ] & \text{Def. of Union} \\
            & \neg (x \in A) \wedge \neg (x \in B) & \text{De Morgan's Law} \\
            & (x \in \overline{A}) \wedge (x \in \overline{B}) & \text{Def. of Complement} \\
            & x \in \overline{A} \cap \overline{B} & \text{Def. of Intersection}
            \end{align}

Since we have shown :math:`x \in \overline{A \cup B} \rightarrow x \in \overline{A} \cap \overline{B}`, we have proven :math:`\overline{A \cup B} \subseteq \overline{A} \cap \overline{B}`.

Now we will show :math:`\overline{A} \cap \overline{B} \subseteq \overline{A \cup B}`