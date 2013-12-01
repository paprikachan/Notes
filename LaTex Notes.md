1. 开始

***

    \documentclass[11pt]{article}
    \begin{document}
    ...
    \end{document}

2. 标题

***

    \title{...}
    \author{...}
    \date{\today}
    \maketitle

3. 章节

***
    \section{...}
    \subsection{...}
    \paragraph{...}
    \part{report style}
    \chapter{book style}
    
3. 数学公式

***

    $$ 2x^{34} $$
    $$ x^33 $$
    $$ x_2 $$
    $$ x_y $$
    $$ \pi $$
    $$ \alpha $$
    $$\beta $$
    $\beta$
    $$ y=\sin{x} $$
    $$ \log_5x{x} + \log_x + \ln_x $$
    $$ \log_{5x}1 $$
    $$\sqrt{2} + \sqrt[3]{2}$$
    $$\frac{x}{y}$$
    $$\displaystyle{\frac{x}{y}}$$
    $$ 3(\frac{2}{3})$$
    $$ 3\left(\frac{2}{3}\right)$$
    $$ \left. \frac{dy}{dx} \right|_{x=1} $$

4. 表格

***

    \begin{tabular}{|c|c|c|c|c|c|}
    \hline
    x & 1 & 2 & 3 & 4 & 5 \\ \hline
    $$f(x)$$ & 10 & 11 & 12 & 13 & 14 \\ \hline
    \end{tabular}

5. 推导公式

***

    \begin{eqnarray*}
    5x^2-9&=&x+3\\
    x^2&=&34\\  
    x&\approx&\pm1.32423
    \end{eqnarray*}

6. 列表

***

    \begin{enumerate}
    \item pencil
    \item paper
    \item tomato
    \item egg
    \end{enumerate}

    \begin{itemize}

    \item pencil
    \item[\#] paper
        \begin{itemize}

        \item plain
        \item ruled

        \end{itemize}
    \item tomato
    \item egg

    \end{itemize}

    \texttt{hahha}

***
