\documentclass[11pt]{article}
\usepackage[a4paper, margin=1in]{geometry}
\usepackage{hyperref}
\usepackage{enumitem}
\usepackage{amsmath}

\title{Explainable AI Under Shortcut Learning}
\author{}
\date{}

\begin{document}
\maketitle

\section{Overview}
This repository contains an experimental notebook investigating the behavior of post-hoc attribution methods under shortcut learning.
Specifically, it examines the divergence between predictive reliance and attribution mass when models exploit spurious or non-causal features.

The primary goal is to assess the epistemic reliability of attribution-based explanations in controlled shortcut scenarios.

\section{Scope}
The experiments focus on:
\begin{itemize}[noitemsep]
    \item Convolutional neural networks trained on synthetic or controlled image data
    \item Parametrized shortcut strength injected during training
    \item Evaluation of classification performance versus attribution behavior
    \item Grad-CAM-based regional attribution analysis
\end{itemize}

This repository is intended as a diagnostic study rather than a benchmarking leaderboard.

\section{Notebook Contents}
The main notebook (\texttt{XAI.ipynb}) includes:
\begin{itemize}[noitemsep]
    \item Dataset generation or preprocessing
    \item Model training under varying shortcut conditions
    \item Attribution extraction using Grad-CAM
    \item Quantitative and qualitative analysis of attribution mass
\end{itemize}

\section{Key Questions}
\begin{itemize}[noitemsep]
    \item Do attribution maps faithfully reflect causal feature usage?
    \item How does shortcut strength affect attribution reliability?
    \item Can high-confidence explanations be misleading under shortcut learning?
\end{itemize}

\section{Requirements}
Typical dependencies include:
\begin{itemize}[noitemsep]
    \item Python 3.8+
    \item PyTorch
    \item Torchvision
    \item NumPy
    \item Matplotlib
\end{itemize}

Exact versions may be specified within the notebook.

\section{Usage}
Open and run the notebook sequentially:
\begin{verbatim}
jupyter notebook XAI.ipynb
\end{verbatim}

Ensure GPU support is enabled if available, as training is computationally non-trivial.

\section{Limitations}
This study is intentionally constrained:
\begin{itemize}[noitemsep]
    \item Synthetic or simplified data
    \item Single-model architecture focus
    \item Post-hoc methods only
\end{itemize}

Results should be interpreted as diagnostic evidence, not universal guarantees.

\section{Citation}
If this repository is used for academic work, please cite it appropriately or contact the author.

\end{document}
