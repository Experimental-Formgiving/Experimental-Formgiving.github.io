---
layout: default
title: "Computational Image Analysis"
has_children: false
parent: "Tools"
nav_order: 1
---

# Introduction

Images consist of pixels, which is data that you can use to quantify relations between pictures. You can also let a computer interpret the content of an image, using some computer vision algorithm. As these algorithms are generally trained in a machine learning context (almost always some kind of deep learning network), they are always biased with respect to the training they received. Take this bias into account when using machine learning (AI).

An accessible introduction is the book [Distant Viewing -
Computational Exploration of Digital Images](https://mitpress.mit.edu/9780262546133/distant-viewing/) which only recently came out and can be freely accessed a MIT Press. In [chapter 2](https://direct.mit.edu/books/oa-monograph/chapter-pdf/2163341/c001100_9780262375160.pdf), the authors explain that before analysing images you first need to extract information, a process they call *annotation* which I rather replace with *computational annotation* as we obviously can also annotate with humans (crowdsourcing could solve a scaling problem and it would still be possible to do 'distant' viewing, i.e. compare a relatively large body of pictures).

# Colab notebooks
We will use python notebooks via [google colab](https://colab.research.google.com). They seem the most versatile tool to share data analysis although the downside is obviously that we rely on big tech. If this choice meets objection we have to find some alternative like [Jupyter](https://jupyter.org) but this will cost considerably more time and effort, and this is only a short course.

Some extra advantages of google colab is that computation happens in the cloud (i.e. you do not need a powerful computer) and many AI (including generative stuff like Stable Diffusion) applications can be run. You probably need to upgrade your account if you want to do heavy computation: a colab pro account is 11 euro's and works quite good (but first check if you really need it), a colab pro+ account is 51 euro's and then you'll have the advantage that you can run them in the background (while closing your browser): not really necessary for this course I think!

## Movieposter colors
The first case study discussed in [Distant Viewing -
Computational Exploration of Digital Images](https://mitpress.mit.edu/9780262546133/distant-viewing/) concerns the design of movie posters, and in particular their usage of colours. Let's try to loosely replicate their analysis.

In this [colab notebook](https://colab.research.google.com/drive/1drDMUUZ6gK2udRu9Frza_XjcNZBmttXD?usp=sharing) I analyse movies posters that I found on [Kaggle](https://colab.research.google.com/corgiredirector?site=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Framan77768%2Fmovie-classifier%2Fdata). Imagedatasets come in all kinds of formats, this one is csv file with image names and their movie genre, and a subfolder with all the images. It looks like this:

![V+D Framework](/images/kagglePandasFile.jpg)

## Average image calculation
An interesting way of finding patterns in image collections is taking the average. Per pixel you literally compute the average value, and you thus need to have images of exactly similar dimensions. Don't worry, the notebook does this for you but be aware that everything gets scaled to a small square image.

[Average image notebook](https://colab.research.google.com/drive/1XdmI7N2V3raNM1o2JFG-VEMJD0MM16vA?usp=sharing)




<!--
Maybe something about latent images, i.e. information about a training set that is latently present in networks.
-->
