
**Important**:
- All text inside \<brackets\> is a placeholder you should replace.
- This tutorial assumes you read [github.md](https://github.com/PolluxSpace/Tutorials/blob/main/tutorials/github.md) or have some pre-existing git/github knowledge.

## Setup your Project on the Pi

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

## Clone repositories on the Pi

Please keep Raspberry Pi files organized by cloning your repositories in `~/repos/`. The following commands already take this into consideration.

You can skip this tutorial if you're using a code editor capable of authenticating into github and cloning repositories.

If the repository is public, you can simply run:

```
cd ~/repos
git clone "https://github.com/<username>/<reponame>.git"
```

For a safer, and more robust cloning command, using PolluxSpace github credentials:

```
cd ~/repos
gh repo clone <username>/<reponame>
```

If the PolluxSpace account doesn't have permission to clone the repo, the command will fail.

If the project is private, you might have to include the PolluxSpace credentials as follows:

```
git remote set-url origin <url>
```

This is the typical url format. You can ask for a auth token to department's Technology Manager, or generate one inside github if you have access to PolluxSpace credentials by following [this guide](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-fine-grained-personal-access-token)

```
url format: https://<username>:<token>@github.com/<username>/<reponame>
pollux url format: https://PolluxSpace:<token>@github.com/PolluxSpace/<reponame>

```

