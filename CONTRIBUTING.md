# Contributing guide

The project for collaborative modelling of the brain grew out of the 2022 Cosyne tutorial. The aim is to work together, openly on a large scale computational brain modelling project. Visit the official website [here](https://comob-project.github.io/). Our first project is a spiking neural network model of sound localization trained using surrogate gradient descent that came out of the [Cosyne 2022 tutorial](https://neural-reckoning.github.io/cosyne-tutorial-2022/) (freely available). Ultimately, the aim is to write a massive joint paper and everyone who contributes will get to be an author of that paper, regardless of whether or not their work is included in the final draft.

Here's how we're currently organizing contributions, although note that this is the first project in the community, so the exact workflow for collaboration is still a work in progress and may change over time.

## Step 1: Get familiar with the project

For background to this project, [check out the freely available Cosyne 2022 tutorial](https://neural-reckoning.github.io/cosyne-tutorial-2022/) and the [introductory notebook](https://comob-project.github.io/snn-sound-localization/main/notebooks/introduction.html) in this project.

You can get a quick feel for the current activity by [starting here](https://comob-project.github.io/snn-sound-localization/main/web/home-page.html). This automatically generated website collates all the parallel subprojects currently underway, listing them in order of how finished they are and how recently they've been modified, so that the most relevant stuff will be at the top.

We will be organizing regular meetings to talk about progress, you might want to come along to these. We'll add a link to those here when we have a regular venue, but for the moment sign up to our [Github Discussions](https://github.com/comob-project/snn-sound-localization/discussions) page and [discord](https://discord.gg/Zpd6RYYyuf) where we'll announce everything.

## Step 2: Pick a problem

We'll try to leave plenty of open questions clearly marked in our notebooks. Does one of them tickle your fancy? If so, check if anyone else is working on it, and if not, dive in!

Make a fork of the repository and start editing your own Jupyter Notebooks in the `notebooks/` folder. You might name the notebook `notebooks/your_name.ipynb`, for example. You
can essentially do whatever you want in your notebook!

## Step 3: Join the community

Once you have something you'd like to show to others and discuss, open a pull request. We'll review your contribution (just to make sure it's not spam, nothing scary), and add you to the Github repository. We'll include your fork as a branch in the repository that you can continue to work on. Your contribution doesn't have to be finished at this point, just enough to want to start showing it and discussing with others. Once it's included in the repository, the current state will start automatically showing up in the automatically generated [JupyterBook](https://comob-project.github.io/snn-sound-localization/main/web/home-page.html).

## Step 4: Interact with the community

Now that your work is visible in the [JupyterBook](https://comob-project.github.io/snn-sound-localization/main/web/home-page.html), others will comment on your work. You can also comment on their work. Join our meetings and discuss the overall direction of the project. [Be nice!](CODE_OF_CONDUCT.md)

As part of this, you might want to join the team that works on refactoring code that is used in several subprojects and generating a reusable Python package. If you're a strong Python user, this might be something you'd enjoy, but it's entirely optional!

## Step 5: Finalise your subproject

The aim is to get your subproject into the final form of a figure or table that can be included in the paper we'll write at the end. Let us know when your subproject gets to this stage by opening a pull request to merge into the main branch. We'll do a more thorough review at this stage, and ask you to cut out any extraneous stuff and refactor a little to use the current version of the shared code to keep it all maintainable.

## Step 6: Help write the paper

Once the story is clearer, we'll start an Overleaf document and start writing up the paper. If you can, please join in on this! Write the paragraph for your subproject. Comment on the overall flow of the text and improve it, etc.

# Technical stuff

## Keeping your branch up-to-date

Since git branches are essentially sequences of commits, it's likely that your personal branch (`your_name/main`) will fall 
behind the commit sequence in the `main` branch. This happens when new commits are added to the main branch.

To keep your branch up-to-date, you should use  `git fetch origin main:main` and `git rebase main` from time to time. The
first command updates your local `main` branch, and the second command incorporates the new `main` commits into your branch,
and then places your commits at the end of the sequence. You shouldn't use `git merge`, because it can lead to
incompatible sequences of commits.

Of course if you need help with any of this, then please ask and someone will help out!

## Writing commit messages

Try to make your commit message informative, without going over ~50 characters. Some of us like to use [Conventional
Commits](https://www.conventionalcommits.org/en/v1.0.0/), which look like `<type>: <message>`. For example, `fix: fixes
a bug with the fano factor algorithm`, or `feat: adds a new figure for cross-correlation`.