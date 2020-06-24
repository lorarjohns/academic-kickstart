---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Mathematics of Computing: Set Theory"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-06-22T19:38:34-04:00
lastmod: 2020-06-22T19:38:34-04:00
featured: false
draft: false
markup: mmark

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

_Author's note: I'll be blogging my way through my graduate coursework in Mathematical Foundations of Computing this semester at Stanford. Follow along for an introduction to abstract mathematics and how it can help you solve problems in computer science._

## What is a set?

A set is an unordered collection of distinct elements.

It doesn't matter if the elements of a given set have different types from one another. The main point is that they must all be __distinct__, and that their order doesn't matter. So $$ \{1, 2, 3\} $$ is the same set as $$ \{2, 3, 1\} $$ which, in turn, is equivalent to $$ \{1, 1, 2, 2, 2, 3, 3\}. $$

## Set notation

To denote a set, write its elements in curly braces. There are two ways to say what elements are in a set. You can list them out explicitly, like we did above. You can even use this convention if the set is infinite, by using __ellipses__ to indicate continuation. For example:

$$ \text{The set of natural numbers } \mathbb{N} \text{ is } \{0, 1, 2, 3, 4, \ldots \}. $$

Alternatively, you can use __set builder__ notation. To use set builder notation, you give a recipe for the set inside the curly braces. For example, we could define the set of all perfect squares as:

$$ \{n^2: n \in \mathbb{N}\}. $$

For sets where the pattern to continue isn't apparent or doesn't exist, set builder notation is a better idea.

# What can sets contain?

Sets can be collections of anything. They can contain numbers, words, cats, memes, or even other sets.

An object is an __element__ of a set if, among the members of that set, one of them is exactly that object.

For example, $$ 1 \in \{1, 2, 3\}, $$

where $\in$ is the symbol that means "is an element of". On the contrary,

$$ 4 \notin \{1, 2, 3\}, $$

where $\notin$ is the symbol that means "is not an element of".

Likewise,

$$ \{1, 2\} \in \{\{1, 2\}, 3\}, $$

because $ \{1, 2\} $ is an object that has an exact counterpart in the set. However,

$$ 1 \notin \{\{1, 2\}, 3\}, $$

because there is no object in the set that __exactly matches__ the object $1$.

## The empty set

The empty set is the set which contains no elements. It is denoted using empty braces: $$ \{\} $$ or the special empty set symbol: $$ \emptyset. $$

For __all__ objects $x$, $x \notin \emptyset$.

The empty set itself can be an element of another set. Let's define a set $S$ as

$$ S = \{\emptyset\}. $$

_Is $S$ equivalent to the empty set?_ __No!__ $S$ is a set that has __one element__ in it, but the empty set has __zero__. The fact that $S$'s only element is the empty set doesn't matter---we can't "look inside" of the elements of sets this way.

## Set operations

You can compare sets in useful ways using basic set operations.

To add sets together, take their __union__:

$$ A \cup B $$

is the set of all the elements in $A$ and all the elements in $B$. So, for example, if we have the sets

$$ A = \{\text{python}, \text{c}, \text{go}\} \\
 B = \{\text{javascript}, \text{rust}, \text{r}\} $$

 then $A \cup B = \{\text{python}, \text{c}, \text{go}, \text{javascript}, \text{rust}, \text{r}\}. $

Set union is equivalent to _logical or_: $$ \{x: x \in A \lor x \in B\} $$ is equivalent to $A \cup B$.

To get _only_ the members that two sets have in common, take their __intersection__:

$$ A \cap B $$

means only those elements that are in _both_ $A$ _and_ $B$. So, if we have the sets 

$$ A = \{\text{python}, \text{c}, \text{go}\} \\
 B = \{\text{c}, \text{go}, \text{r}\} $$

then $A \cap B = \{\text{c}, \text{go}\}$.

Set intersection is equivalent to _logical and_: $$ \{x: x \in A \land x \in B \} $$ is equivalent to $ A \cap B $.

If two sets have nothing in common, then their intersection is the empty set. So, for example, if we have the sets

$$ A = \{\text{python}, \text{c}, \text{go}\} \\
 B = \{\text{javascript}, \text{rust}, \text{r}\} $$

 then $ A \cap B = \emptyset $, because these sets have no elements in common.

Set __difference__ tells you what elements are in one set that don't appear in the other. So, for example, if we have the sets

$$ A = \{\text{python}, \text{c}, \text{go}\} \\
 B = \{\text{c}, \text{go}, \text{r}\} $$

then $ A\setminus B = \{\text{python}\}$ . Be careful, because unlike union and intersection, set difference is not a _symmetric_ operation:

$$ B \setminus A = \{\text{r}\}, $$

a different result from $A \setminus B$.

The set difference $ A \setminus B$ is logically equivalent to $\{x: x \in A \land x \notin B\}$.

## Logic and Vacuous Truth

It's important to wrap your head around the way formal logic works.

First, let's define a couple of terms to help us talk about logic. A __predicate__ is a statement that is either true or false. The statement $x < 0$ is either true or false for any given $x$. "Is this statement logical?" is not a predicate, because it is a question, and cannot be either true or false.

When we talk about formal logic here, we'll mostly be discussing [first-order logic](https://github.com/OpenLogicProject/forallx). There are other systems, including intuitionist logic, in whit statements may be neither true nor false. But those don't apply here.

Now, remember the empty set, $\emptyset$. Is the empty set a subset of any other set $S$?

By the definition of a subset, $$\emptyset \subseteq S \text{ if every element of } \emptyset \text{ is an element of } S. $$

But there aren't any elements in $\emptyset$. So is the predicate "$\emptyset$ is a subset of $S$" true or false?

On the one hand, since there are no elements of $\emptyset$ in $S$, you might be tempted to say it is false. But on the other hand, you can't find any examples of an element of $\emptyset$ that _isn't_ in $S$.

__Vacuous truths__ are statements that are meaninglessly true, because they don't actually prove relevant to the instance at hand.

A statement of the form $P \rightarrow Q$ is always true if $P$ is always false. Likewise, "All $X$ are $Y$" is vacuously true if there are no $X$.

So the statement, "If we are on Venus, then the sun is exploding" is true.

As a result, $\emptyset$ is a subset of (any!) $S$, because "every element of $\emptyset$ is an element of $S$" is a vacuous truth, so the conditional statement "if every element of $\emptyset$ is an element of $S$, then $\emptyset$ is a subset of $S$" is also vacuously true.

That is a bit to wrap your head around, so think about it and come back for the next post on power sets, Cantor's Theorem, and how these relate to the limitations of computability.
