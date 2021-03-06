General tips:

* Always use microtype
* Don't use " as quotes. Use \`\`..'' instead. This way the quotes will actually render asymmetrically, as they should.
* Remember to put a space after punctuation. This is just a general editing tip though.
* Whenever writing something like "N (N <= 10)", use something like $N$ ($N <= 10$). This puts proper spaces in. Also it is more logical -- the parentheses aren't "math parentheses".
* Don't forget the \paragraph{...} command. Most often, replacing the lowest level of subsection with paragraphs results in a prettier document.
* \\footnotemark is useful -- inline footnotes are often difficult to edit.
* Use the \url command for urls.
* \\itemize within \\itemize looks really cool, makes custom bullets.
* I prefer not using the `\par` command if at all possible. Just leave an empty space -- it more clearly shows the paragraph in source code, and avoids needless commands.
* This is a rather obscure bug fix, but often if spacing after a command, adding a `{}` after the command, or a `%` (if it's at the end of a line) fixes it.
* I usually use `interfootnotelinepenalty=10000000` or something like this, it tries to force footnotes to be on the same page where they are mentioned.

Math tips:

* Remember that math is part of the sentence. So one should punctuate after an equation, even if it in display mode.
* Don't forget to use display mode (\\[...\\]) whenever an equation becomes long, or especially tall.
* Even though * is used to represent multiplication, it looks not the best -- I prefer \\times or just nothing at all.
* Use \left and \right around parentheses for tall math objects, e.g. \\left( \\frac{1}{2} \\right)
* The amsthm package is completely indispensable.
* Don't put empty lines before and after display mode! This makes all the indentation and spacing wrong.
* The equation environment is good for labelled equations; it puts a number like (14), which can then be referenced. Within this the aligned environment can be used for multiline equations which can be made to align at = signs. On the other hand, this disallows putting interline explanatory notes, like with align*.
* The \\underbrace command is quite nice, it allows you to explain what a certain part of an equation is.
* When making commands to be used in math mode, use \\ensuremath. For instance `\newcommand{\R}{\ensuremath{\mathbb{R}}}`.
* If one wants a multicharacter italic variable name, do not just write the letters in math mode. For instance, if we want an italic "count" variable, do not write, for example, `2count + 1`. Rather, write `2\mathit{count} + 1`. Otherwise the kerning is wrong. This explains why: http://logophile.org/blog/2006/09/05/latex-math-mode-and-italics.
* If one has an enumeration of several math formulas within text, like "a = 1, b = 2, c = 3 and d = 4", prefer `$a = 1$, $b = 2$, $c = 3$ and $d = 4$`, not `$a = 1, b = 2, c = 3$ and $d = 4$`. This allows LaTeX to split the enumerated items.
* This website is enormously helpful for finding commands for making various symbols: http://detexify.kirelabs.org/classify.html.
* This website is very helpful for making category theory diagram: https://tikzcd.yichuanshen.de/.
* I have almost always found the `\allowdisplaybreaks` command to be good -- it allows long equations to split between pages.

Tikz:

* Tikz is, in my opinion, rather unpleasant to work with. However, I've found it useful more than once to write scripts that automatically generate tikz diagrams.

Some good lstlisting settings:

```
\lstset{%
    basicstyle=\footnotesize,%
    escapeinside={\%}{)},%
    extendedchars=true,%
    frame=single,%
    keepspaces=true,%
    keywordstyle=\color{blue},%
    language=c++,%
    morekeywords={*,...},%
    numbersep=5pt,%
    numberstyle=\tiny\color{mygray},%
    rulecolor=\color{black},%
    showspaces=false,%
    showstringspaces=false,%
    showtabs=false,%
    stepnumber=2,%
    stringstyle=\color{mymauve},%
    tabsize=2,%
    title=\lstname%
}%
```
