
Tip: All text inside \<brackets\> is a placeholder you should replace.

Before following this tutorial, make sure to read [github.md](https://www.youtube.com/watch?v=HkdAHXoRtos).

## Get started with your project in a Raspberry Pi

Start your project by creating a virtual environment for it.

A virtual environment (venv) is a localized python instance, with its own version and installed packages. This allows different projects in the same raspberry to have different and maybe incompatible python versions and packages installed, without any problem.

In a terminal, create your project's venv by running this command.

```
python3 -m venv ~/envs/<venv-name>
```

Now, whenever you need to perform an action in a terminal that relates to your project, like installing packages or running scripts, you must "source" that venv. To do that, run the following command:

```
source ~/envs/<name>/bin/activate
```

Whenever you're running code directly in a code editor, you must also specificy what venv it must use, otherwise it will just use the default python interpreter, without any of the libraries you installed. In vscode, for example, you select your venv by doing CTRL+SHIFT+P > Interpreter > \<venv-name\>

## Clone a repository within your Raspberry Pi's terminal

To clone a repo, perform the following command (this will use the default PolluxSpace github credentials):
```
cd ~/repos
gh repo clone <username>/<reponame>
```
If the PolluxSpace user doesn't have permission to clone the repo, the command will fail.

If the project is private, pulling from it must have our credentials. As such, we must add them to the origin. Here's how:

```
git remote set-url origin <url>
```

This is the typical url format. Ask the key to your technology manager, or generate one using PolluxSpace credentials directly in github.

```
url format: https://<username>:<key>@github.com/<username>/<reponame>
pollux url format: https://PolluxSpace:<key>@github.com/PolluxSpace/<reponame>

```

