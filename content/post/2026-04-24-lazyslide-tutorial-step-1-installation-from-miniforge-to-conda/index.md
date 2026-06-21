---
title: 'LazySlide Tutorial: Step 1 Installation from miniforge to conda'
author: R Build
date: '2026-04-24'
slug: lazyslide-tutorial-step-1-installation-from-miniforge-to-conda
categories: []
tags: []
editor_options: 
  markdown: 
    wrap: 72
---

Miniforge installed Python 3.13 as your base (newest version). But
lazyslide depends on spatialdata, which hasn't caught up to Python 3.13
yet --- it still needs Python 3.10--3.12. This is exactly why conda
environments exist. You don't install project packages into base. You
create a separate mini-environment with the right Python version for
each project.

The fix --- create a dedicated environment for lazyslide: Run these
three commands one at a time:

-   **Create an environment with Python 3.12**

```
conda create -n lazyslide python=3.12 -y
```

This makes a new isolated environment called lazyslide with Python 3.12.
Takes ~30 seconds.

-   **Activate it**

```
conda activate lazyslide
```

Your prompt will change from (base) to (lazyslide) --- that means you're
now inside the environment.

1.  Install lazyslide

    ```
    conda install -c conda-forge lazyslide -y
    ```

    This will now succeed because Python 3.12 satisfies the dependency
    chain.

2.  **Install jupyter in this environment:**

    ```         
    conda install -c conda-forge jupyter -y
    ```

So, now Every time you want to work with lazyslide:

**Step 1: open Terminal and run:**

```         
conda activate lazyslide
```

**Step 2:**Launch Jupyter**

```         
jupyter notebook
```
