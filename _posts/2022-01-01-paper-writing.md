---
layout: post
title: Paper Writing Tips
date: 2022-01-01 09:00:00-0800
description: Some tips and suggestions when writing academic papers.
comments: false
---

## Main documents
- [ ] Long sentences (say more than 3 lines) must be split.
- [ ] When you want to excuse something or want to describe something, which breaks a logic a little bit, use a footnote. This is a very useful technique.
- [ ] When you have an important message try to emphasize them in different sections like abstract, intro, experiments, etc. It is okay to rephrase and be redundant in the message as reviewers might not read every section in detail but still, they have to get the message. (Added on 3-May-2019)
- [ ] Try to make the paper concise: some parts can be safely removed when they are isolated with the main message of the paper and following discussion. (Added on 07-Oct-2020)
- [ ] Include as many back-pointer (i.e., refer to previous content such as equation number or section number when discussing new stuff) in the paper as possible. Those help you to make each section of the paper tighter and reduce the difficulty for others reading your paper. (Updated on 07-Oct-2020)

## Tables and Figures
- [ ] Do not simply copy the figure from other papers (including your previous papers). It breaks the copyright and also gives very negative impressions to the reviewer.
- [ ] Make Tables and Figures self-consistent. For example, add a brief experimental design and sometimes brief discussions in the caption. If it uses some abbreviations, also explain the abbreviation even if it is described in the main body or other tables & figures. (Updated on 07-Oct-2020)
- [ ] Try to put figures and tables on the bottom or top of the page and avoid including in the middle of the document as much as possible but there can be exceptions. (Added on 3-May-2019)
- [ ] Wherever possible in figures, refer to respective variables in equations and be consistent with the notation. (Added on 3-May-2019)
- [ ] Try to categorize the table entry and use `\hline` to separate them when the table is complex. (Added on 07-Oct-2020)

Reviewers are super busy, and they may only check the abstract, figures, tables, and would make some decisions.

## Equations
- [ ] Equations are like figures. This makes the paper look more scientific. Please try to put basic equations even if you think it is trivial
- [ ] Use `algorithm.sty` to describe the algorithm. This also makes the paper look more scientific
- [ ] Do not duplicately use the same characters for different variables
- [ ] Distinguish the type of variables/values (e.g., scalar $x$, vector $\mathbf{x}$, matrix $\mathbf{X}$, sequence $X$)
- [ ] Add the domain when you introduce a new variable, e.g., $$X = (\mathbf{x} _t \in \mathbb{R} ^D| t=1, \cdots, T)$$ with $X = (\mathbf{x} _t \in \mathbb{R} ^D| t=1, \cdots, T)$ with the explanation, e.g., $$X$$ is a $$T$$-length sequence of $$D$$-dimensional speech features.
- [ ] Equations must not have any mistakes.
- [ ] When you want to distinguish some variable with some descriptions, use superscript with non-italic font (e.g., Cross entropy loss with $$\mathcal{L}^{\text{ce}}$$, MSE loss  with $$\mathcal{L}^{\text{mse}}$$)
- [ ] Some operations must be non-italic (e.g., $max()$ -> $\max()$, $sigmoid()$ -> $\text{sigmoid}()$, $BiLSTM()$ -> $\text{BiLSTM}()$
- [ ] Avoid paragraph breaks after equations. (Added on 3-May-2019)

## Abbreviations
- [ ] Add definition when they appear first. (even for trivial words like HMM, ASR)
- [ ] Add some back-pointer when using them so that reader can easily go back to check the definition. (Added on 07-Oct-2020)

## Grammar check
- [ ] Use some auto-grammar check (MS word or grammarly)

## References
- [ ] Try to list more than 25 references (more references give the impression that this paper performs a good survey in this area)
- [ ] Put balanced references across several research groups. Reviewers, who are assigned to one paper, are usually from different institutes.
- [ ] It is very good to cite your (or your colleagues') papers to increase the visibility of you and your colleagues.
- [ ] but be careful about the above balance issue, and always try to include competitors' references.
- [ ] Please clean up/normalize the reference. If you simply paste the reference from Google Scholar BibTex, it would include a lot of noises
- [ ] be careful about the capitalization in the title of the BibTeX, e.g., `HMM` should be `{HMM}`.
- [ ] cite the published version instead of the arxiv version (we can use https://github.com/yuchenlin/rebiber)

## When you get comments from your colleagues or reviewers
- [ ] Try to reflect all comments. If they point out something wrong or their points are based on misunderstanding, which is still your fault. Some of your documents just confuse them. Please make sure to fix them.
- [ ] If someone points out some issues, please make sure that these points may be applied to the other parts of the document. When they point out one issue, please try to fix all related parts in the whole document.

## Experimental discussions
- [ ] Try to make a story and a message, it's not interesting to read plain descriptions of the experimental results without them. We don't need details, but some overall trends to get the message. (Added on 3-May-2019)
- [ ] Try to make connections between different paragraphs/subsections in the discussion. (Added on 3-May-2019)
- [ ] When there are many experiments to be presented, it's a good idea to explain each experiment with their results instead of discussing the experimental settings and result separately. (Added on 07-Oct-2020)
- [ ] If your experiments are worse than those of the other reports, please emphasize the excuse (e.g., footnote or other clear remarks in the table/figure). The reviewers often missed the detailed conditions, and they judged only with the numbers. If there are clear remarks, we can avoid such misjudgements.