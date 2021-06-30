# Multi-line-equation-by-beamer
Many people use LaTeX mainly for its ability to generate good-looking and consistent mathematical equations. As a LaTeX documentclass, beamer can further help to make frames and slides for presentations, where no problem for single-line euqations. However, after many tests, I believe that the following way is the only reasonable one for presenting a multi-line equation line by line with beamer, with no additional manual effort. 

By defining 

      \newcommand{\pauseditem}{\pause \item[]}

it can be done as 

      \begin{frame}
      ...
      \begin{itemize}
      \begin{eqnarray}
            (first line of the equation ending with \\)
            \pauseditem  (second line of the equation ending with \\)
            \pauseditem  (third line of the equation ending with \\)
              ...
            \pauseditem  (last line of the equation without ending \\)
      \end{eqnarray}
      \end{itemize}
      ...
      \end{frame}

Although some error messages would be reported during compiling the LaTeX file, the slides can be generated properly. As in the last frame of the example, the lines of the equatioin is increasingly shown with the slide runs, and all equal signs are aligned and equation numbers are generated for each line automatically. 

Supposing one would like to copy such equations to a file for LaTeX article editing later, the effect of all "\pauseditem" can be nulled by redefining "\newcommand{\pauseditem}{}". 

Furthermore, this LaTeX example file also sets 16:9 screen, text and background colors, and article-look equation.


