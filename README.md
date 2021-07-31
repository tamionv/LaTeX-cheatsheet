General tips:

* Don't use " as quotes. Use \`\`..'' instead. This way the quotes will actually render asymmetrically, as they should.
* Remember to put a space after punctuation. This is just a general editing tip though.
* Whenever writing something like "N (N <= 10)", use something like $N$ ($N <= 10$). This puts proper spaces in. Also it is more logical -- the parentheses aren't "math parentheses".
* Don't forget the \paragraph{...} command. Most often, replacing the lowest level of subsection with paragraphs results in a prettier document.
* \\footnotemark is useful -- inline footnotes are often difficult to edit.
* Use the \url command for urls.
* \\itemize within \\itemize looks really cool, makes custom bullets.

Math tips:

* Remember that math is part of the sentence. So one should punctuate after an equation, even if it in display mode.
* Don't forget to use display mode (\\[...\\]) whenever an equation becomes long, or especially tall.
* Even though * is used to represent multiplication, it looks not the best -- I prefer \\times or just nothing at all.
* Use \left and \right around parentheses for tall math objects, e.g. \\left( \\frac{1}{2} \\right)

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
