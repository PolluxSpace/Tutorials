## Create a Repository
A repository is like a google drive for your code, that controls all the history of changes made to it. Make sure to keep it private. To create one follow these steps:

1. log into PolluxSpace's github account from within your prefered browser.
2. Follow this guide: [create repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository). An external guide is used to make sure the procedure is up to date. Please don't forget to keep this repository private.
3. [Add your team's github accounts as collaborators](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository). You should never edit code as PolluxSpace. If a team member doesn't have a github account, they should create one using their personal e-mail and not the polluxspace.pt one.

## Use a Repository
To use a repository, you must clone it into your computer. Think of it like logging into google drive in a computer, and editing files from there.

Follow this guide: [Cloning a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).

Now, you should plan with your team a strategy for developing code, like which branches do what, to minimize merge conflicts, and start developing!

### If you're unfamiliar with Git or Github
There's a high probability you or your team members won't have any experience using git or github. Make sure to get a basic understanding before advancing. If no-one from your team knows git or github, please talk with your directive body to request a workshop.

If you just need a refresher, here's the most important concepts:

Git is a source control program. It keeps track of a folder and all its subfolders. Github is a cloud storage provider (like google drive), specifically made for Git and to host folders with code in it.

A repository is a fancy word for folder that git is controlling.

Repositories have branches, which are named copies or version of your repository. By default, a repository has one main branch, but you can create and delete branches, as well as merge between them in different ways. This is useful to keep a stable main branch while the team does various experimentations in other branches. You can even have a main experiment branch, of which specific experiment branches come from. It's also useful so multiple people can be changing code without affecting the other person's ability to save that code and show it to everyone else remotely.

When you clone your repository, you're essentially fetching all the branches that are on github (called remote branches), and making copies of them with the same names (local branches).

When you change code in your computer, it's not automatically updated on github. Instead, you have to first define which files you've changed and wrte a small descriptive message of that change. That's called a "commit". You can commit onto a local branch, and then "push" your commit to the remote branch.

Also, unless your code editor is already periodically doing this for you (which isn't recommended), the code on github doesn't get updated automatically in your computer, so you won't see changes made by other people. For that, you must "fetch" from the remote, and then "merge" any changes onto the branch you're working on. You can do this all in one step by executing a "pull"

All the names in quotations are actual commands you can execute on your terminal, but git and github become much more powerful when integrated into a code editor. Here's some more complete tutorials:
- [without using the terminal](https://www.youtube.com/watch?v=8Dd7KRpKeaE) 
- [using the terminal](https://www.youtube.com/watch?v=HkdAHXoRtos) 