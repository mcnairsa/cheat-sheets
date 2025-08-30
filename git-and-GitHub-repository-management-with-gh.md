# Common actions using git and 'gh', the GitHub command line tool.

## Notes:
- This guide relates to working on the command line.
- It is assumed you are familiar with the commands'cd', 'ls', 'mkdir', 'rm', 'mv' & 'cp'.
- '% ~/projects': It is assumed you have a directory called 'projects' that lives inside your home directory.
    - On Windows command this is typically: > C:\Users\<your-username>>\projects\ e.g.: C:\Users\sam\projects
    - On 'nix-based systems (Mac, GNU/Linux, BSD &c) this is typically: ~ projects % 
    - '%' is the *command prompt*. Commands below are written thus: % cd ~/projects.
        This means:' at the command prompt, type 'cd ~/projects@ (without the quotation marks) and press 'Enter'.
    - '~' means your (the current user's) home directory 
- All work is done in a directory *within* ~/projects/ unless otherwise stated.
- 
### Common or Every Day Actions

[ToDo but do all this from 'nix box]
## git status
[show screenshot]
[add command]

## git add

## git commit

## git push 



## Occasional Actions

### Create a repository on GitHub from an existing local repository:
1. Open a terminal or command prompt.
2. Navigate to the directory where you want to create the repository.
2.a. Note: This means you need to be in the directory above the one where you want to create the repository. This is because the `gh repo create` command creates a new repository in the current directory.
~~3. Run the command `git init` to initialize a new repository.~~
4. Create a new file called `README.md` and add some content to it.
5. Run the command `git add .` to stage all changes.
6. Run the command `git commit -m "Initial commit"` to commit the changes.
7. Run the command `git remote add origin <repository_url>` to add a remote repository.
8. Run the command `git push -u origin master` to push the changes to the remote repository.
9. Run the command `git branch -M main` to rename the master branch to main.
10. Run the command `git push -u origin main` to push the changes to the remote repository.

#### Additional steps:
11. Run the command `git checkout main` to switch to the main branch.
12. Run the command `git branch -d master` to delete the master branch.
13. Run the command `git push origin --delete master` to delete the master branch on the remote repository.
14. Run the command `git push -u origin main` to push the changes to the remote repository.


### Create a local repository and a remote repository on GitHub using the GitHub CLI:
1. Install the GitHub CLI by following the instructions on the GitHub CLI website.
2. Log in to GitHub by running the command `gh auth login`.
3. Create a new repository by running the command `gh repo create`.
3.a-1. You can name the repository with `gh repo create <repository_name>` but if you give it a name you'won't be creating the local and remote repositories interactively.
3.a. Note: Follow the prompts to create a new repository on GitHub.
3.b. Note: The process will assume that you don't already have a local repository.
3.c. Note: If there is no README.md file and you want to create it maybe uses the description of the repository that you gave earlier.
4. Add the remote repository to the local repository by running the command `git remote add origin <repository_url>`.
4.a. Note: The <repository_url> will be something like https://github.com/<username>/<repository_name>.
5. Push your local repository to the remote repository by running the command `git push -u origin main`.


### Create a local copy ['clone'] of a remote repo e.g. from GitHub
1. cd to the ~/projects/ directory
2. Run the command: % 

Steps to connect to a remote repository on GitHub using the GitHub CLI:
1. Install the GitHub CLI by following the instructions on the GitHub CLI website.
2. Run the command 'gh auth status' to check the status of your authentication.
3. Log in to GitHub by running the command `gh auth login`.
4. Add the remote repository to the local repository by running the command `git remote add origin <repository_url>`.
5. Fetch the remote repository by running the command `git fetch origin`.
6. Merge the remote repository into the local repository by running the command `git merge origin/main`.
7. Push your local repository to the remote repository by running the command `git push -u origin main`.

Steps to delete a remote repository on GitHub using the GitHub CLI:
1. Install the GitHub CLI by following the instructions on the GitHub CLI website.
2. Run the command 'gh auth status' to check the status of your authentication.
3. Log in to GitHub by running the command `gh auth login`.
3.a Note:  to run the `... delete ...` command, you need to have the necessary permissions. If you don't the delete will fail with a message telling you how to grant yourself the necessary permissions. You may have to authorise your device to access your account. Follow the white rabbit... er ... prompts.
4. Delete the remote repository by running the command `gh repo delete <repository_name>`.
5. Confirm the deletion by typing `y` and pressing Enter.
E0ED-6C13
Steps to remove a remote origin from a local repository using the GitHub CLI:
1. Install the GitHub CLI by following the instructions on the GitHub CLI website.
2. Run the command 'gh auth status' to check the status of your authentication.
3. Log in to GitHub by running the command `gh auth login`.
4. Remove the remote origin by running the command `git remote remove origin`.
