# Publishing Workflow

Let's make our work public to share it with the world. Use this power wisely and **within legal laws & regulations** (no hate, no bullying, misinformation etc.).

Note: This was last updated in **July 2021**. At this time...
    
* ...the settings for github pages are located at: tab **settings** / sub menu **pages**. 
* ... Github's default branch name currently is `main`. This changed during time. If you want to publish older repositories, or use older versions of the command line tool you may need to rename the old `master`-branch with `git branch -m main` before following this guide.

## Idea

We will use Github's service Github pages to publish content of repositories to a publicly accessible URL in the shape of https://accountname.github.io/repositoryname/. 

There are some things you need to be aware of:

1. github pages by default translates markdown files (like README.MD) to HTML while using a program called [Jekyll](https://jekyllrb.com/). We want to write our own HTML/CSS, so we will disable this default behavior.
2. github pages only works for public repositories for basic accounts. (PRO accounts also can publish private repositories)


## Instructions

1. Create a repository on your own personal GitHub account
    * if you have a free github account, the repository needs to be **public** for this exercise
2. Copy the adress of your repository and clone it locally to your maschine with `git clone yourCopiedLink`.
3. Create an `index.html` file as a starting point and fill it with some boilerplate code (e.g. a document title and a first level heading `<h1>Hello public world</h1>`)
4. make an initial commit by staging (`git add index.html` and `git commit -m "initial commit"`)
    * you _can_ push the `main` branch to github with `git push origin main`
    * (this step is _optional_, because we will use another branch)
5. By default Github pages with a branch `gh-pages`
    * let's create such a branch as a copy of the current (`main`) by typing `git checkout -b gh-pages` on the terminal.    
6. Push the new branch to the remote github repository with `git push origin gh-pages`.
7. Enable GitHub Pages for the repository.
    * See the settings tab of your repository, on the left navigate to the sub menu **Pages** ![settings](settings-pages.jpg)
    *  set "gh-pages" as the live branch and /(root) as the live directory. ![branch](settings-select-branch.jpg)
    * Github will show the URL of your public page on top of the Source section. It will look like https://youraccount.github.io/repositoryname/
    * If you follow the link now, you will see a rendered version of the repository's readme.md (if you checked that option, during the creation of the repository) or an error message telling that there is nothing to display.
8. Deactivate Jekyll.
    * you can turn **off** the default behavior (of translating markdown files to HTML) by creating a file names `.nojekyll` in the directory that you selected to be published.
    * create such a file with VSC or the terminal by typing `touch .nojekyll` in the terminal. Be aware of the dot (`.`) in front of the filename
9. Submit this change to github
    * stage the changes in the directory with `git add .`
    * make a new commit with `git commit -m "added .nojekyll`
    * push it to remote with `git push origin gh-pages`
10. Visit the public URL (like https://youraccount.github.io/repositoryname/) of and check if everything works like it should.