---
{"dg-publish":true,"permalink":"/website-pages/encode/","tags":["assumed","formal/category-theory","formal/logic/proof-theory","story","Encode"],"noteIcon":"images/Greek_uc_delta_icon.svg","created":"2026-03-28T12:06:22.427+00:00","dg-note-properties":{"tags":["assumed","formal/category-theory","formal/logic/proof-theory","story","Encode"],"Links":["[[2024-11-21_23-46-33_Perplexity.ai_In Meaning in Dialogue]]","[[2024-11-21_23-52-13_Perplexity.ai_Briefly explain the sharded DLT proposed for the Xi'an]]","[[Story]]"],"note-icon-1":null}}
---


This is a mock-up showing a PDF that highlights the principle that logical elements should be selectable in queries and interim results.
<?xml version="1.0" encoding="UTF-8"?><svg width="88" height="100" version="1.1" xmlns="http://www.w3.org/2000/svg"> <path d="m1.0424 99 42.958-98h2.4023l40.555 98zm69.03-6.0057-28.616-70.372-30.947 70.372z"/></svg>

# Intelligibility - Defeasibility
#### Rule 1. Formation
$$\frac{\\\;\\\; \vdash X : \mathrm{Type} \\\quad\\\quad x:X \vdash A(x):\mathrm{Type}\\\;}
     {\vdash \sum_{x:X} A(x) : \mathrm{Type}\\\\}
$$

Where $\vdash$ means from this assumption
and from the form
$$
\frac{\text{premises}}{\text{conclusion}}
$$
where in the premise there is no initial assumption.

No initial assumption is ***indefeasible***.

In terms of the subtlety of logical elements, contrast this with the way the turnstile changes direction on this website's landing page, here [[ΑΒΓΔ.XYZ\|ΑΒΓΔ.XYZ]].
The following is mock-up output from the parse of a positive sequent tree showing the groups extracted from some of the four rows. I had to edit this by hand as AI and code still makes many errors.

<iframe src="/img/user/resources/01301_sequent_segmentation_corrected_01.pdf#toolbar=0&navpanes=0&view=FitH" width="100%" height="400px"></iframe>

***This is the compiled source for the complete positive sequent tree.***


```tikz
\usepackage{amsmath, amssymb}
\usepackage{tikz-cd}
\usetikzlibrary{positioning}

\begin{document}


% Entailsbar Macro (Parameterized)
\newcommand{\entailsbar}[4]{% #1 = node name, #2 = height, #3 = vertical offset, #4 = line thickness
  \ensuremath{\mkern-1mu}% Space before entails-bar
  \pgfmathsetmacro{\halfheight}{#2/2} % Calculate half the height
  \draw[thin, line width=#4] (#1.south)++(0.1em+#2/4,#3) ++(0,#2) -- ++(0,-#2); % Left vertical
  \draw[thin, line width=#4] (#1.south)++(0.1em+#2/4+#2/2,#3) ++(0,#2) -- ++(0,-#2); % Right vertical
  \draw[thin, line width=#4] (#1.south)++(0.1em+#2/4,#3+\halfheight) -- ++(#2/2,0); % Horizontal
  \ensuremath{\mkern-1mu}% Space after entails-bar
}

% Spaced Symbol Macro
\newcommand{\spacedsym}[1]{\mkern-0.4mu #1 \mkern-0.4mu}  % Adjust 3mu as needed

% Define Node Content Terms (for easier modification)
\newcommand{\Gpa}{\ensuremath{\scriptstyle\spacedsym{;} \spacedsym{\Gamma^{+}} \spacedsym{,} \spacedsym{\alpha^{+}}}}
\newcommand{\Gpb}{\ensuremath{\scriptstyle\spacedsym{;} \spacedsym{\beta^{+}}}}
\newcommand{\Gakahb}{\ensuremath{\scriptstyle\spacedsym{\alpha^{+\# \stackrel{h}{2}}} \spacedsym{\beta^{+}}}}
\newcommand{\Gaka}{\ensuremath{\scriptstyle\spacedsym{;} \spacedsym{\alpha^{+}}}}
\newcommand{\Gpbs}{\ensuremath{\scriptstyle\spacedsym{;} \spacedsym{\Gamma^{+}} \spacedsym{,}\spacedsym{\beta^{+}}}}
\newcommand{\Gps}{\ensuremath{\scriptstyle\spacedsym{;\sigma^{+}}}}
\newcommand{\Gakabhs}{\ensuremath{\scriptstyle\spacedsym{;} \spacedsym{\beta^{+\# \stackrel{h}{2}}} \spacedsym{\sigma^{+}}}}
\newcommand{\Gp}{\ensuremath{\scriptstyle\spacedsym{;} \spacedsym{\Gamma^{+}}}}
\newcommand{\Gs}{\ensuremath{\scriptstyle\spacedsym{;} \spacedsym{\sigma^{+}}}}

\begin{tikzpicture}[scale=1.5, node distance=.09cm, every node/.style={scale=1.2}]

  % *** Row 1 ***
  % Sequent Group 1.1
  \node (G11) at (-1.5,0) {\Gpa};
  \node (G111) at (-1.07,0) {}; % Helper node for entailsbar positioning
  \entailsbar{G111}{0.3cm}{0.0cm}{0.3pt}
  % Sequent Group 1.2
  \node (G12) at (-0.52,0) {\Gpb};
  % Underline
  \draw[thin] (-2.1,-0.18) -- (0.1,-0.18);

  % *** Row 2 ***
  % Sequent Group 2.1
  \node (G21) at (-1.5,-1) {\Gp};
  \node (G211) at (-1.35,-.9) {}; % Helper node for entailsbar positioning
  \entailsbar{G211}{0.3cm}{-0.1cm}{0.3pt}
  \node (G22) at (-0.3,-0.9) {\Gakahb};
  % Sequent Group 2.2
  \node (G23) at (0.8,-1) {\Gp};
  \node (G231) at (1.0,-.9) {}; % Helper node for entailsbar positioning
  \entailsbar{G231}{0.3cm}{-0.1cm}{0.3pt}
  \node (G24) at (1.6,-1) {\Gaka};
    % Sequent Group 2.3
  \node (G25) at (2.85,-1) {\Gpbs};
    \node (G251) at (3.3,-.9) {}; % Helper node for entailsbar positioning
  \entailsbar{G251}{0.3cm}{-0.1cm}{0.3pt}
  \node (G26) at (3.9,-1) {\Gps};
  % Underlines
  \draw[thin] (-1.9,-1.18) -- (1.9,-1.18);
  \draw[thin] (2.3,-1.18) -- (4.1,-1.18);

  % *** Row 3 ***
  % Sequent Group 3.1
  \node (G31) at (-1.5,-2) {\Gp};
    \node (G311) at (-1.36,-1.9) {}; % Helper node for entailsbar positioning
  \entailsbar{G311}{0.3cm}{-0.1cm}{0.3pt}
  \node (G32) at (-0.82,-2) {\Gpb};
  % Sequent Group 3.2 
  \node (G33) at (0.53,-2) {\Gp};
    \node (G331) at (0.64,-1.9) {}; % Helper node for entailsbar positioning
  \entailsbar{G331}{0.3cm}{-0.1cm}{0.3pt}
  \node (G34) at (1.72,-1.9) {\Gakabhs};
  % Underline
  \draw[thin] (-1.9,-2.18) -- (2.4,-2.18);

  % *** Row 4 ***
  % Sequent Group 4.1
  \node (G41) at (-1.5,-3) {\Gp};
  \node (G411) at (-1.35,-2.9) {}; % Helper node for entailsbar positioning
  \entailsbar{G411}{0.3cm}{-0.1cm}{0.3pt}
  \node (G42) at (-0.82,-3) {\Gs};

\end{tikzpicture}
\end{document}

```
Diagram adapted from James Trafford, _Meaning in Dialogue: An Interactive Approach to Logic and Reasoning_ (Springer, 2017), p. 186.

I come to AI from psychoanalysis. With over three decades of clinical work shaping how I think about language, change, and responsibility. In an alternative career that I pursued for about a decade, I was an object‑oriented Java back-end specialist.
My roles were in industry, but I also taught software engineering at the University of Greenwich for a year.
My goal is to build a neurosymbolic architecture in which agentic AI systems act only as untrusted proposal generators around a formally specified, co‑constructive logic kernel with explicit provenance and experimental, optional cryptographic anchoring. The aim is to give research communities in mental health, AI safety, and software engineering a way to represent and revise their claims, norms, and disagreements as evolving logical structures, and to add tools for transparent, auditable reasoning in scientific and clinical practice, where the assessment of critical risk is essential.

The Encode fellowship’s combination of compute, mentorship, and access to ARIA‑adjacent ecosystems would enable me to move from conceptual design to large‑scale experiments. With substantial compute and access to corpora such as Mathematics for Safe AI, Safeguarded AI, and neighbouring AI‑safety, clinical literature and relevant training data, I would use this architecture to map how notions of risk, alignment, harm, and responsibility are introduced, contested, and stabilised across communities. This connects model‑level safety work to the higher‑level question of how societies and expert groups actually reason about, and modify, their processes and beliefs in the context of powerful AI systems.

This fellowship could later grow into an open research commons or, if there is sufficient demand and fit with ARIA’s mission, the nucleus of a focused research organisation dedicated to epistemic and provenance infrastructure for agentic AI.

The technical project I am most proud of is the design of a “logic‑centric” agent architecture that treats AI assistants as untrusted front‑ends to a formally specified proof engine. AI assistant‑agents are wrapped around a typed sequent‑calculus core: a co‑constructive proof/refutation kernel that accepts only structured inputs and produces checkable proof objects, while all free‑text interaction is mediated by an “agentic edge” that can suggest but never alone ratify inferences. A provenance layer, maintaining sequential order, records formulas, sequents, proofs, and their “supports/refutes/alternative” relations back to source documents, so that any reasoning step can be re‑checked. Each agent has its own internal logic and interface, and interactions between agents become compositional transformations between their local theories. At an early stage, this can be prototyped as an Obsidian‑integrated research tool.

I value this work because it demonstrates a concrete neurosymbolic alternative to treating large models as opaque authorities: it shows how to separate suggestion from endorsement and make epistemic commitments explicit and auditable.
Substantial compute would enable two forms of stress‑test.
1. Running large‑scale experiments over evolving bodies of work—such as AI‑safety literature or software artefacts—to see how formal guarantees and cryptographic commitments can constrain what AI tools “claim”.
2. Employing methods like those in Karpathy's Autoresearch (Claude.md manifest) that iterate over alternative engine and prompt configurations, defining success for experimental purposes.

I would therefore stress‑test this design by running large‑scale experiments over evolving bodies of work (such as AI‑safety literature or software artefacts) to see how formal guarantees and cryptographic commitments constrain what AI tools are allowed to “claim”, and by using autoresearch‑style methods to systematically explore engine and prompt configurations under clearly defined success criteria.

I have had a cross‑disciplinary career. I have over thirty years’ experience as a psychoanalytic practitioner, and around ten years as an object‑oriented Java engineer, including teaching software engineering at the University of Greenwich. More recently, my work has brought me into contact with AI‑safety researchers, category theorists, and clinicians interested in computational tools.

The project itself is explicitly cross‑disciplinary: it models expert communities as evolving “local topoi”, drawing on category theory, social choice, game theory and information theory, while remaining grounded in the ethical and epistemic constraints of psychoanalytic and clinical practice. I am comfortable translating between conceptual languages (clinical, mathematical, and engineering) and designing structures where different communities’ internal logics can interact without being reduced to a single crude metric.

## Know what I want to build
Use the 12 months to build and stress‑test a “logic‑centric” agentic research assistant, initially as a proof‑of‑concept integrated into tools like Obsidian or similar research environments. The core idea is to separate suggestion from endorsement: language‑model‑based agents can propose claims, links, and arguments, but all logically significant steps must pass through a formally specified, co‑constructive proof/refutation kernel that produces checkable proof objects and explicit provenance. This would allow individual researchers and small teams to see not just what an AI system says, but also how its suggestions relate to prior claims, what evidence it relies on, and where the uncertainties and open questions lie.

Deliver three things in the year: (1) a minimal, well‑specified logical kernel and provenance schema that can host multiple internal logics (e.g. intuitionistic, co‑constructive, modal); (2) an agent orchestration layer that treats different tools and communities as “local topoi” with their own signatures, so that interactions between them are compositional and inspectable; and (3) a working prototype that can be used on real corpora, starting with AI‑safety, safeguarded‑AI, and related scientific literatures.
To build a small but solid infrastructure that makes epistemic commitments explicit and auditable, and that can later be scaled up—whether as an open research commons, a specialised safety tool, or the seed of a more formal, focused research organisation.