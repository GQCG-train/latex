---
marp: true
paginate: true
style: |
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
  }
---

# **LaTeX**
## a cog in a reproducible research framework

---

# Why (not) LaTeX

<div class="columns">
<div>

## Pro

* **Flat text**
* Stability needed for large documents
* You don't have to control formatting

</div>
<div>

## Con

* Only as strong as the weakest member of your research community
* It is very hard to control formatting
* You need to get used to an ecosystem of different tools

</div>
</div>

Current advice: only use LaTeX when absolutely needed!

---

# Tutorial 1: the UGent beamer template

- Download [UGent beamer](https://github.com/GQCG-oss/ugent-beamer) template.
- Reopen the root folder in a container.
- Cmd/Ctrl+Shift+P > LaTeX Workshop: Build LaTeX project.

---

- Add a slide: 

```latex
\begin{frame}
\frametitle{Sample frame title}
This is some text.
\end{frame}
```

- Add a figure:
```latex
\includegraphics{media/screenshots/screenshot-0.png}
```

Go through the template and consult the [docs](https://www.overleaf.com/learn/latex/Beamer) for more information.

---

# What did we just do?

<div class="columns">
<div>
We have started our journey on the road to reproducible research.

We are now at the *environment* stage:
* Docker
* Git
* Conda

Made possible by user-friendly interfaces: 

* VSCode (.devcontainer)
* Github (intro to issues and PRs)

Is possible for **any** environment (i.e. **Python**, **R**, ...)! 

</div>
<div> 

![width:500px](img/tutorials_overview.png)

</div>
</div>

---

# Use case: spin diagrams

Want to **fully** reproduce one of our latest papers? Download our [spin-diagrams repo](https://github.com/GQCG-res/spin-diagrams) and 
* open the `notebooks` to reproduce/extend our results using Python
* open the `paper` folders to adjust our papers

Do not have enough compute: meet the cloud: [Github Codespaces](https://github.com/features/codespaces).

---

# Tutorial 2: thesis template

- Download the [GQCG Cleanthesis](https://github.com/GQCG-oss/cleanthesis) template.
- Reopen the root folder in a container.
- Cmd/Ctrl+Shift+P > LaTeX Workshop: Build LaTeX project.

<G|QC|G> *forked* this project to extend it and, eventually, contribute back. We are open to issues and PRs!

---

# Use case: Bookdown and Knowdes

However, standard LaTeX classes are **not** always the way to go. 

We want to have access to the Wikipedia of Electronic Structure Theory.

Meet [Knowdes](https://gqcg-res.github.io/knowdes/), powered by [Bookdown](https://bookdown.org/). 

This is a HTML interface, but you can export the same document to a **PDF**, **EPUB** and **Word**.

---

# Some questions

- *As intended by Microsoft*, leaving the Office Ecosystem is hard. Why?
- `LaTeX vs Word` should be viewed in a wider context: what are the most important documents for *you* and *your group*? Do they need to be kept **agile**?
- These slides were made with [Marp](https://marp.app/), which support math TeX code (e.g. $\hat{H} \ket{\Psi} = E \ket{\Psi}$). I did **not** use beamer. Why? 
- Note that **one** click that is not *captured* can break reproducibility! Why is this a bad thing?
- You **can** draw [chemical structures](https://mirror.koddos.net/CTAN/macros/generic/chemfig/chemfig-en.pdf) in LaTeX, but I don't know if you should?