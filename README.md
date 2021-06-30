# Multi-line-equation-by-beamer
Many people use LaTeX mainly for its ability to generate good-looking and consistent mathematical equations. As a LaTeX documentclass, beamer can further help to make frames and slides for presentations, where no problem for single-line euqations. However, for presenting a multi-line equation line by line, I did many tests with \begin{itemize} ... \item ... \end{itemize} in \begin{eqnarray} ... \end{eqnarray} environments, but failed. Now I am clear that \pause does it straightforwardly, as shown in the following and the slides of the last frame in the example.

By defining 

      \newcommand{\pauseditem}{\pause}

it can be done as 

      \begin{frame}
      ...
      \begin{eqnarray}
            (first line of the equation ending with \\)
            \pauseditem  (second line of the equation ending with \\)
            \pauseditem  (third line of the equation ending with \\)
              ...
            \pauseditem  (last line of the equation without ending \\)
      \end{eqnarray}
      ...
      \end{frame}

To define and use \pauseditem, rather than \pause directly, is for the situation, where supposing one would like to copy such equations in the beamer to a regular LaTex file for article editing later, all "\pauseditem" can be "removed" by redefining "\newcommand{\pauseditem}{}". 

Furthermore, this LaTeX example file also sets 16:9 screen, text and background colors, and article-look equation.


