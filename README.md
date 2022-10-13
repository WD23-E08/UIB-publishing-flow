# Publishing Workflow
[![Status overview badge](../../blob/badges/.github/badges/autograding/badge.svg)](#-results)


Let's make our work public to share it with the world. Use this power wisely and **within legal laws & regulations** (no hate, no bullying, misinformation etc.).

We will use Github's service **Github pages** to publish content of repositories to a publicly accessible URL in the shape of https://accountname.github.io/repositoryname/. 


## Prerequisites
Make sure that you have admin access to this repository. This is needed in order for you to enable GitHub pages.
## Instructions

1. Create an `index.html` file as a starting point and fill it with some boilerplate code (e.g. a document title and a first level heading `<h1>Hello public world</h1>`)
2. Enable GitHub Pages for this repository.
    * See the settings tab of your repository, on the left navigate to the sub menu **Pages** ![settings](settings-pages.jpg)
    *  set `main` as the live branch and /(root) as the live directory. ![branch](settings-select-branch.jpg)
    * Github will show the URL of your public page on top of the Source section. It will look like https://youraccount.github.io/repositoryname/
3. Visit the public URL (like https://youraccount.github.io/repositoryname/) of and check if everything works like it should.

## CodeBuddy not seeing your deployed page?
* Go to the actions tab
* Click on the title of your last commit
* Select 'Re-run action'

## Bonus: Helper package gh-pages from npm

There is an NPM package `gh-pages` that helps to automate steps for updating your published page, while working from main or other branches.

You may want to install it globally on your system with `npm install -g gh-pages@3.0.0`, to avoid adding a package.json to very basic small projects with pure HTML/CSS.

With the package you can work on your main branch or others, and control what directory you want to publish to the gh-pages branch and become public.

### Call example.

Let's assume you work from the root of your main branch and want to put all it's content into the gh-pages branch and publish it, type:

```bash
gh-pages -d ./
```

You can also decide to specify another sub-directory to become the root of the publication.

```bash
gh-pages -d dist
```

This is useful if you use development tools (like sass) to produce a `/dist/` directory (=distribution) for publishing from other source files.

The content of the subdirectory will become the content of the **root** of the `gh-pages` branch

[//]: # (autograding info start)
# <img src="https://github.com/DCI-EdTech/autograding-setup/raw/main/assets/bot-large.svg" alt="" data-canonical-src="https://github.com/DCI-EdTech/autograding-setup/raw/main/assets/bot-large.svg" height="31" /> Results
> ⌛ Give it a minute. As long as you see the orange dot ![processing](https://raw.githubusercontent.com/DCI-EdTech/autograding-setup/main/assets/processing.svg) on top, CodeBuddy is still processing. Refresh this page to see it's current status.
>
> This is what CodeBuddy found when running your code. It is to show you what you have achieved and to give you hints on how to complete the exercise.


### Publishing Workflow

|                 Status                  | Check                                                                                    |
| :-------------------------------------: | :--------------------------------------------------------------------------------------- |
| ![Status](../../blob/badges/.github/badges/autograding/status0.svg) | index.html file exists and contains `h1` element |
| ![Status](../../blob/badges/.github/badges/autograding/status1.svg) | Should return status code 200 |



[🔬 Results Details](../../actions)
[🐞 Tips on Debugging](https://github.com/DCI-EdTech/autograding-setup/wiki/How-to-work-with-CodeBuddy)
[📢 Report Problem](https://docs.google.com/forms/d/e/1FAIpQLSfS8wPh6bCMTLF2wmjiE5_UhPiOEnubEwwPLN_M8zTCjx5qbg/viewform?usp=pp_url&entry.652569746=UIB-publishing-flow)


[//]: # (autograding info end)