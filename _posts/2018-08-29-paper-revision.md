---
title: 'What I Learn from Paper Revision'
date: 2018-08-29
permalink: /posts/2018/paper-revision/
tags:
  - writing
  - research
---

Paper writing is a crucial point for research, and I'm pretty bad at it. From my first paper experience, I learned a lot (mostly from my advisor) during paper revision. My bullets are as follows.

Paper organization:

* Write a list of contributions as the last paragraph of introduction. This will catch readers attention, to what's important in this paper. Also add "forward references" to specific sections.

* Always write something in between \section and \subsection. It'll serve as an essential logical connection between the proceeding and following. 

* Try to discover the logical order between sections, and arrange it the way most naturally. The usual ordering of paper is: introduction -> preliminary -> existing problems -> methods -> experiments.

* Don't write "related work" right after introduction. "Related work" isn't essential to the paper.

* Merge similiar figures and tables for simplicity and saving spaces.


Language:

* Pay special attention to the symbolic consistency

* For different terms, name them significantly different to reduce confusion


Latex skills:

* Attach this line to each latex file (to collaborate with modern latex editor):

```latex
!TEX root = main.tex
```

* Define phrases that appear in the math equation as a command, and use \mathit or \mathrm to wrap it up (otherwise, it's ugly).

* Use \centering instead of "center" environment.

* Use \\! to save space between math symbols

* Use \url{} or \hyperref for the URL footnote, and move it after the period.

* Use \\\\[0.2cm] to provide vertical spaces in addition to \vspace{0.2cm}

* Save capital letter ($Y$) for matrices or nonterminals, use bold one ($\mathbf{y}$) to represent a sequence, and lower-case one ($y$) to denote tokens.


Space saving skills:

* Use \vspace{-0.5cm} to reduce the space between figure and its caption.

* "respectively" -> "resp."

* $a$=0 instead of $a=0$

* Figure 1 -> Fig. 1; Table 1 -> Tab. 1; Section 1 -> Sec. 1 etc..

There're definitely a lot missing. I'll try to update this list in the future.