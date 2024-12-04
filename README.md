# CodePod User Study

This manual will guide you through the features of CodePod IDE and the steps to
follow to complete the user study.

## Introduction to CodePod IDE

CodePod IDE is a Scalable Jupyter Notebook.

We'll use the term code "pods" to refer to the code pieces/blocks. It is
equivalent to the code "cells" in Jupyter.

![CodePod IDE](./assets/best-practice.png)

The major new features over Juptyer notebooks are:

1. A Canvas-based interface (UI)
   - Unlike Jupyter's linear notebook, in CodePod, you can move the code blocks
     freely in 2D space.
2. Oragnize your code in nested scopes
   - You can group logically related code blocks into a scope. Scopes can be
     nested.
3. Scope Semantics
   - Not only can you organize pods with scopes, they also have semantic
     meanings to help you isolate namespaces in the runtime.
4. Def-use visualization
   - If a code pod uses symbols defined in another code pod, there will be an
     edge from the definition pod to the usage pod. The symbol def-use includes
     variable, functions and classes.

At the end of the study, you will be asked to evaluate how useful these features are.

## The CodePod App in the cloud

CodePod is a web app. The test server is at https://test.codepod.io. You can
login with your Google account and start using it right away. All code are saved
in the cloud and executed in the cloud runtimes.

Please refer to the [user manual](https://codepod.io/docs/manual/) for how to use the app.

## Step 1: Do the User Study

The goal is to understand the pros and cons of the CodePod IDE compared to
Jupyter.

We prepared three Jupyter notebooks. **Your task** is to test the three projects
on both Jupyter notebook and on CodePod to understand both tools, and then
complete the questionare.

- To use CodePod, go to https://test.codepod.io.
- To use Jupyter, you can install Jupyter notebook or use VSCode's Jupyter extension.

You are also welcome to try other projects on CodePod if you wish.

The three jupyter notebooks:

- Fashion MNIST classification with pytorch ([1-fashion-mnist.ipynb](1-fashion-mnist.ipynb))
- Python web scraping using beautifulsoup ([2-web-scraping.ipynb](2-web-scraping.ipynb))
- Kaggle competition: sentiment analysis on Amazon food review data ([3-amazon-review.ipynb](3-amazon-review.ipynb))

We'll also provide reference projects in CodePod. You can either view it before
or after your own try. It is recommended to try it before viewing the reference
design.

## Step 2: Complete the Questionaires

This questionare is in its early development. You are encouraged to give rough
feedback drafts. We are planning to do a few round of feedback loops, (i.e.,
eval, feedback, discuss, eval & feedback again) to develop the questionaire and
try to address concerns about the tool.

Please complete the three jupyter notebooks in CodePod to get familiar with
CodePod. Then, when you are ready, please evaluate CodePod with the following
questionaires.

### Q1: Scalability

Please estimate how many code blocks

- The number of pods (cells) that you are comfortable to develop in Jupyter: e.g., 100
- The number of pods that you are comfortable to develop in CodePod: e.g., 100

What is the factors backing your estimation of scalability?

- For Juptyer: ...
- For CodePod: ...

Your comments related to scalability: ...

### Q2: Ablation Study

CodePod IDE introduces several features over Jupyter notebook. Please evaluate
how useful they are compared with vanilla Jupyter in the score of 0 to 10.
Assuming that 5 is the baseline score of Jupyter. Therefore, the score 0 means
CodePod is significantly worse than Jupyter, and 10 means CodePod is
significantly better than Jupyter.

- Score 1: Overall usefulness of CodePod.
  - Your score (0-10):
- Score 2: The usefulness of the 2D canvas interface and Canvas navigation.
  - This feature includes the ability to freely place code blocks (e.g., side-by-side instead of linear), zoom in and out to view details and bird eye overview.
  - Your score (0-10):
- Score 3: The usefulness of Nested Scope and Semantic Scoping Rules.
  - This feature includes the ability to group related code blocks in scopes for clear organization, hierarchical nested scope, and the runtime semantic namespace separation and API exports during code execution.
  - Your score (0-10):
- Score 4: The usefulness of def-use visualization.
  - Your score (0-10):

### Q3: Time Spent to Organize the Notebooks on CodePod

Please estimate the time spend to transform and organize the jupyter notebook onto CodePod.

Migrating Jupyter notebooks to CodePod requires the following steps.

1. Importing: the notebook is imported to CodePod where all code blocks are orderred linearly.
2. Layouting: Then, users would layout the code blocks on the 2D canvas with the guidance of def-use edges.
   2.1 Scoping: When necessary, developers group logically related code into modules, embed lower-level modules inside higher-level ones, and mark the interfaces (APIs) between modules with the \texttt{\#export} tags.
3. Execution: After the layout and scoping is done, developers can run the code blocks and observe results.

Please enter your estimation in the table below (assuming that you are familiar with how to use CodePod):

| Notebooks             | Fashion-MNIST | Amazon Food Review | Web Scraping |
| --------------------- | ------------- | ------------------ | ------------ |
| number of code blocks | 15            | 40                 | 20           |
| Lines of Code (LoCs)  | 130           | 133                | 110          |
| Time estimation (min) |               |                    |              |

### Q4: time and distance to navigate and udpate code during development

On Jupyter, a large amount of development time is often spent on navigating code
blocks back and forth, e.g., "spend lots of time jumping around".

In this question, we ask developers to estimate the distance of related code
blocks to edit in a develop session, and the time required to navigate to the
targeting code block to edit.

- Distance of co-edit blocks: please estimate how far away are two code blocks that are related.
  - The distance is measured by the number of steps to go from one block to another.
  - E.g, on Jupyter, it is if two blocks have 3 other blocks between them, the distance is 4.
  - E.g., on CodePod, if two pods are next to each other, the distance is 1; for longer distance, please estimate the distance on the 2D Canvas.

| App                                         | Jupyter | CodePod |
| ------------------------------------------- | ------- | ------- |
| Distance of co-edit blocks (number)         |         |         |
| Time to navigate to block-to-edit (seconds) |         |         |

### Other

What you like about CodePod over Jupyter?

- ...

What you like about Jupyter over CodePod?

- ...

What you dislike about CodePod?

- ...

Any other comments?

- ...

Any suggestions to add into this questionaire?

- ...
