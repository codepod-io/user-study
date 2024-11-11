# CodePod User Study

Version: v0.1 (2024-11-11)

This manual will guide you through the features of CodePod IDE and the steps to
follow to complete the user study.

## Introduction to CodePod IDE

CodePod IDE is a Scalable Jupyter Notebook.

In CodePod IDE, the code "pods" are the code pieces on the canvas. It is
equivalent to the code "cells" in Jupyter.

The major new features over Juptyer notebooks are:

1. A Canvas-based interface (UI). Unlike Jupyter's linear notebook, in CodePod, you
   can move the code blocks freely in 2D space.
2. Oragnize your code in arbitrarily nested scopes. You can group logically
   related code blocks into a scope. Scopes can be nested.
3. Scope Semantic
   1. Each scope is in a separate namespace. All variables, functions and
      classes are only visible inside the scope (including its children
      scopes).
   2. A pod can be marked `public`, which extends its visibility into its
      parent scope.
4. Def-use visualization. If a code pod uses symbols defined in another code
   pod, there will be an edge from the definition pod to the usage pod. The
   symbol def-use includes variable, functions and classes.

## The CodePod App in the cloud

CodePod is a web app. The test server is at https://test.codepod.io. You can
login with your Google account and start using it right away. All code are saved
in the cloud and executed in the cloud runtimes.

Please refer to the [user manual](./Manual.md) for how to use the app.

## User study

The goal is to understand the pros and cons of the CodePod IDE compared to
Jupyter.

We prepared three Jupyter notebooks. **Your task** is to test the three projects
on both Jupyter notebook and on CodePod to understand both tools, and then
complete the questionare.

- To use CodePod, go to https://test.codepod.io.
- To use Jupyter, you can install Jupyter notebook or use VSCode's Jupyter extension.

You are also welcome to try other projects on CodePod if you wish.

The three jupyter notebooks:

- Fashion MNIST classification with pytorch ([fashion-mnist.ipynb](fashion-mnist.ipynb))
- Kaggle competition: sentiment analysis on Amazon food review data ([amazon-review.ipynb](amazon-review.ipynb))
- Python web scraping using beautifulsoup ([web-scraping.ipynb](web-scraping.ipynb))

We'll also provide reference projects in CodePod. You can either view it before
or after your own try. It is recommended to try it before viewing the reference
design.

## Questionaire

This questionare is in its early development. You are encouraged to give rough
feedback drafts. We are planning to do a few round of feedback loops, (i.e.,
eval, feedback, discuss, eval & feedback again) to develop the questionaire and
try to address concerns about the tool.

Scalability

- The number of pods (cells) that Jupyter scales to: e.g., 100
- The number of pods that CodePod scales to: e.g., 100

What is the factors backing your estimation of scalability?

- For Juptyer: ...
- For CodePod: ...

Organizability and Clearity

- Does the features of CodePod help with organizing the code? E.g., the def-use visualization, the Canvas interface, the nested scopes.

What you like about CodePod over Jupyter?

- ...

What you like about Jupyter over CodePod?

- ...

What you dislike about CodePod?

- ...

Any other questionaire items to add?

- ...
