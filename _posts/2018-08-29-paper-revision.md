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

* Write a list of contributions as the last paragraph of introduction. This will catch readers attention, to what's most important in this paper. Also add "forward references" to specific sections.
* Always write something in between \section and \subsection. It'll serve as an essential connection between the proceeding and following. And it'll largely help the logical flow.
* Try to discover the logical order between sections, and arrange it the way most naturally. The usual ordering of paper is: introduction -> preliminary -> existing problems -> methods -> experiments.
* Don't write "related work" right after introduction. "Related work" isn't essential to the paper.
* Merge similiar figures and tables for simplicity and saving spaces.

Language:

* "we can/could observe" -> "we observe"
* Pay special attention to symbol consistency, and name differently (\gr and \lr) to reduce confusion

Latex skills:

* Define phrases that appear in the math equation in the def.tex, and use \mathit or \mathrm to wrap it up.
* Don't use \\begin{center}..\\end{center}, use \centering instead.
* Use \\! to save space between math symbols
* Use \url{} or \hyperref for the URL footnote, and move it after the period.
* `` ` ```` ` ``something`` '' ``  instead of  `` " ``something`` " ``
* Use \\\\[0.2cm] to provide vertical spaces between resizeboxes.

Space saving skills:

* Use \vspace{-0.1cm} to reduce the space between figure and its caption.

* Use "resp." instead of "respectively"

* $a$=0 instead of $a=0$

* Figure 1 -> Fig. 1

There're definitely a lot more writing skills missing. I'll try to update this list in the future.