---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "On Mathematical Notation and Communication in Machine Learning"
subtitle: "Why the linguistics of mathematics matters in programming and tech"
summary: ""
authors: []
tags: []
categories: []
date: 2020-04-07T10:46:09-04:00
lastmod: 2020-05-25T13:22:52-04:00
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

#### Why the linguistics of mathematics matters in programming and tech

**DataSeries highlight:**

*   Math is, at its heart, a language. And language is a human creation, highly expressive but full of assumed background knowledge and fuzzy meanings. This article goes on the relationship between the way we write math and programming and tech.

Mathematicians are fond of saying that mathematical notation is unambiguous.

Explain this, then.

Let this be Figure 1:

$$ 3 \frac{1}{3} $$

<!-- ![image](/post/on-mathematical-notation-and-communication-in-machine-learning/images/1.gif) -->
<!-- Notation for a mixed number -->

And let this be Figure 2:

<!-- ![image](/post/on-mathematical-notation-and-communication-in-machine-learning/images/2.gif) -->

$$ 3x $$

<!-- Notation for an algebraic expression -->

Figure 1 is made up of the elements $ \{3, \frac{1}{3}\}  $. Figure 2 is made up of the elements $ \{3, x\} $. In both, the notation consists of writing the two elements next to each other. For each of these expressions, what is the operation between its elements?

If your answer for Figure 1 is “addition” and for Figure 2 is “multiplication”, how did you know how to evaluate them differently, given that the notation is the same?

</br>

Math is, at its heart, a language. And language is a human creation, highly expressive but full of assumed background knowledge and fuzzy meanings.

Different fields — probability, statistical mechanics, computer science, economics, machine learning — develop their own dialects and idioms. Not only do the _metalinguistic_ labels for mathematical objects vary across disciplines, so do the forms of the objects themselves.

**_Metalinguistic._** _Definition._ Language used to talk about language.

**_Example:_** The term “ [_one-hot_](https://en.wikipedia.org/wiki/One-hot)”, as in “one-hot encoded variable”, comes from digital circuit design. It means “a group of bits among which the legal combinations of values are only those with a single high (1) bit and all the others low (0)”. “One-hot” is a metalinguistic_label for the expressions “00000001”, “00000010”, and “00010000”.

However, the ambiguity of mathematical language is not just in the metalanguage. Here’s an example in which the metalanguage and the notation itself both produce ambiguity: a _double factorial_ and a _semifactorial_, written _n!!_, are the same thing. But _n!!_ is not equal to _(n!)!_, and _double_ means four times as much as _semi-_.

**_Double factorial._** _Definition._ The product of all the integers from 1 up to _n_ that have the same parity (odd or even) as _n_. Also known as the _semifactorial_.

**_Example:_** The semifactorial for evens, odds, and 0:

$$n!! = \begin{cases} \prod_{k=1}^{\frac{n}{2}}(2k) = n(n-2)(n-4)\ldots(4)(2), & \text{ if }n\text{ is even,} \\\\
\prod_{k=1}^{\frac{n+1}{2}}(2k-1)=n(n-2)(n-4)\ldots(3)(1), & \text{ if } n \text{ is odd,} \\\\
1, \text{ if }n=0.\end{cases}$$

For instance:

$$ 7!! = (7)(5)(3)(1) = 105. $$

In other notation:

{{< gist lorarjohns a21013286bac139ad1601f27f50a86a2 >}}

</br>

![image](https://cdn-images-1.medium.com/max/800/0*v4mSaTpJn5Hj5aO3)

Enrico Fermi, legendary physicist. Much of machine learning math tacitly draws from statistical mechanics. (Photo: [Science in HD](https://unsplash.com/@scienceinhd?utm_source=medium&amp;utm_medium=referral))

If you’ve ever studied any discipline whose basis is math, no one ever told you that you were learning a foreign language, but you were. Math evolved alongside human speech for thousands of years, in the mouths and pens of pure and applied mathematicians in Asia, India, Mesopotamia, Europe, Africa, Mesoamerica. Why would it be any less complex or barnacled with age than Sanskrit, Arabic, Latin, Chinese, or English?

That students are not informed of this linguistic task makes learning all the harder, contributes to math anxiety, and serves to keep them out of an expanding set of science and technologically-based fields. Women and minorities comprise a disproportionally small cohort of [STEM students and workers](https://www.pewsocialtrends.org/2018/01/09/women-and-men-in-stem-often-at-odds-over-workplace-equity/). Technologically based jobs pay [dramatically higher wages on average](https://www.pewresearch.org/fact-tank/2018/01/09/7-facts-about-the-stem-workforce/) at every education level. And STEM jobs go unfilled — not because there’s a lack of interest, but because there’s a lack of people who speak the language.Yet, among those who are fluent in mathematics, there exist some who prefer to keep the group of speakers small and difficult to enter. For some groups, mathematical notation is a shibboleth, used to protect their elite status and build their professional cachet.

**_Shibboleth._** _Definition_. a phrase, word, or custom that serves as password, self-identification, sign of affinity, or enforcer of segregation.

**_Example:_** _“If you’re on any tech support call, you can say the code word ‘shibboleet’ at any point and you’ll be automatically transferred to someone who knows a minimum of two programming languages.”_
Other shibboleths in this comic: the Tux doll, the posters of a subway map and a “bearded dude with swords”, and the cargo pants are all markers of a “geek” in-group.

</br>

![image](/post/on-mathematical-notation-and-communication-in-machine-learning/images/5.png)

[Tech Support](https://www.xkcd.com/806/)

Math is often used as such a shibboleth, to regard people with contempt when they struggle to decode the ideas behind the notation. Data scientists and programmers are hardly unique in this regard —for hundreds of years, lawyers in England protected the elite status of the legal profession by making it inaccessible to anyone who did not speak [Law French](https://en.wikipedia.org/wiki/Law_French).

Unlike Law French, though, mathematics is the [language of the universe](https://www.quora.com/Where-did-Galileo-say-Mathematics-is-the-language-with-which-God-has-written-the-universe?share=1). Math is not only the foundation of the algorithms that drive our programs and the science that describes our world and lives. Math is creativity and play, art and humor. It has surprised and delighted human beings the world over throughout history, so much so that we keep inventing it — more accurately, rediscovering it — again and again. We can’t help ourselves. Francis Su makes the case that [mathematics is a matter of human flourishing](https://www.quantamagazine.org/math-and-the-best-life-an-interview-with-francis-su-20170202/).

Language itself is essential to human flourishing. Consider this story of [a deaf man](https://neuroanthropology.net/2010/07/21/life-without-language/) who grew up with hearing parents who could not teach him sign language, who did not understand even the concept of language until he was twenty-seven years old, when a woman mimicked both sides of a conversation for him, and he made the connection between [signifier and signified](https://oregonstate.edu/instruct/theory/signs.html):

> And then he started — it was the most emotional moment with another human being, I think, in my life so that even now, after all these years, I’m choking up — he started pointing to everything in the room. All of a sudden, this twenty-seven-year-old man-who, of course, had seen a wall and a door and a window before-started pointing to everything. He pointed to the table. He wanted me to sign table. He wanted the symbol. He wanted the name for table. And he wanted the symbol, the sign, for window.

> The amazing thing is that the look on his face was as if he had never seen a window before. **_The window became a different thing with a symbol attached to it. But it’s not just a symbol. It’s a shared symbol._** He can say “window” to someone else tomorrow who he hasn’t even met yet! And they will know what a window is. **_There’s something magical that happens between humans and symbols and the sharing of symbols._** 

> **_That was his first “Aha!”_** He just went crazy for a few seconds, pointing to everything in the room and signing whatever I signed. Then he collapsed and started crying, and I don’t mean just a few tears. He cradled his head in his arms on the table and the table was shaking loudly from his sobbing. Of course, I don’t know what was in his head, but I’m just guessing he saw what he had missed for twenty-seven years.

A life without language is not human. We have a fundamental need to cultivate our curiosity, to assign meaning to ideas, and to exchange them with our fellow humans via shared symbols. The medium of exchange is always language. And when the ideas are mathematical, then we invent a mathematical language to help us communicate.

</br>

![image](https://cdn-images-1.medium.com/max/800/0*pbvM99yNLUd9yCIu)

Does the language you speak shape your thoughts? (Photo: [Dmitry Ratushny](https://unsplash.com/@ratushny?utm_source=medium&amp;utm_medium=referral))

In the 1930s, a pair of linguistic anthropologists, Sapir and Whorf, proposed a theory that your mental capability is limited by the language you speak. In its strong form, it is called linguistic determinism, and it says that if your language doesn’t have a word for a concept, then you are cognitively incapable of grasping that concept. It was (and in some circles, remains) a popular view of the world, which many people have used to justify their superiority over others.

**_Linguistic determinism._** _Definition_. The idea that language and its structures limit human knowledge and thought processes, like categorization, perception, and memory.

**_Example:_** In the Hopi language, verbs have no tense markers for past, present, or future. Therefore, Hopi people have no concept of linear time.

Saying certain groups of people are just “[not as good at math](https://www.nytimes.com/2018/08/07/opinion/stem-girls-math-practice.html)” because they haven’t already learned its syntax and vocabulary is the same kind of thing. It effects a gatekeeping mechanism on every field that requires math as the lingua franca for exchanging information. It tells underrepresented groups that if they aren’t fluent already, then they’re not invited to come learn, because they wouldn’t understand anyway.

To the contrary, “[languages, of course, are human creations, tools we invent and hone to suit our needs](https://www.wsj.com/articles/SB10001424052748703467304575383131592767868).” The notation we invent to hold mathematical ideas proves the opposite of the Sapir-Whorf theory: it is thought that shapes language, motivating novel uses of old writing systems, drawings, colors, and clever substitutions to show the chain of logic that leads from hypothesis to conclusion.

[Rainbow Proof Shows Graphs Have Uniform Parts](https://www.quantamagazine.org/mathematicians-prove-ringels-graph-theory-conjecture-20200219/)


There’s a weak form of the Sapir-Whorf hypothesis, linguistic influence, that says that the language you speak _influences_ the way you think. While you are not limited by it, as per linguistic determinism, language can shape or change your perspectives on the information you receive.

**_Linguistic influence._** _Definition_. The idea that language does not determine cognition, but it does influence human knowledge and thought processes.

**_Example:_** A group of people was shown a racially ambiguous photograph of a man and then asked to draw his face. Half of them were told that the picture was of a “Black man”, and the other half were told it was of a “White man”. The half who were told the picture was of a Black man drew more exaggerated, racially stereotypical features than the other group.

Kenneth E. Iverson’s Turing Award Lecture, “[Notation as a Tool of Thought](https://www.jsoftware.com/papers/tot.htm)” explores this weaker linguistic relativism (though, fittingly, in different words):

*   “Mathematical notation provides perhaps the best-known and best-developed example of language used consciously as a tool of thought.”
*   “Nevertheless, mathematical notation has serious deficiencies. In particular, it lacks universality, and must be interpreted differently according to the topic, according to the author, and even according to the immediate context.”
*   “Programming languages, because they were designed for the purpose of directing computers, offer important advantages as tools of thought. Not only are they universal (general-purpose), but they are also executable and unambiguous.”
*   “Executability makes it possible to use computers to perform extensive experiments on ideas expressed in a programming language, and the lack of ambiguity makes possible precise thought experiments.”

We use mathematical notation to create ideas and construct new views of old problems. We build bridges of symbols to carry a train of thought from theorems to proofs. But as Iverson notes, the notation is different according to the topic, author, and even the immediate context. Perhaps that’s why so many people find it less intimidating to start with programming — then fall speechless when they run up against the math behind the code.No one speaks math as a first language. We have all acquired it non-natively, somewhere along the way. The only way to acquire another language is exposure and repetition. Even those who are fluent in it now were beginners at some point.

Learners need access to the raw materials of language — to the texts, yes, but also to the speakers, who provide live feedback. If you’ve ever tried to learn French from a book, then converse with a Parisian, you know that self-study alone will not produce fluency. Silent consonants are difficult to learn in French, but the problem as it pertains to the tangle of opaque symbols scattered across math, engineering, and computing disciplines is daunting to navigate alone.

Language is for communication, after all. It is meant to include, not exclude. We owe it to each other to [create a welcoming culture to make everyone feel like they belong in math](https://www.quantamagazine.org/math-and-the-best-life-an-interview-with-francis-su-20170202/), to translate clearly when we write our own notation, and to teach each other to speak the language at the core of our lives and livelihoods.

Every human being is born capable of learning to speak any human language. There’s no reason to think we have any less capacity to acquire mathematics.
