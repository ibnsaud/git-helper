# Git commands instruction

- [git youtube course](https://www.youtube.com/playlist?list=PLDyvV36pndZFHXjXuwA_NywNrVQO0aQqb)

- [git reference manual](https://git-scm.com/docs)

> ## **1. Set user configurations: git config**

![git config hierarchy](src\git_config.png)

- set username/email for local project:

```sh
git config --local user.name <put_your_name> <put_your_email>
```

- set global username/email for all projects of current user:

```sh
git config --global user.name <put_your_name>/<put_your_email> 
```
- set system username/email for all users:

```sh
git config --system user.name <put_your_name>/<put_your_email>
```

- show git configurations:

```sh
git config --list
```

- remove local parametres:

```sh
git config --unset <user.name> or <user.email>
```

- remove section user:

```sh
git config --remove-section user
```


> ## **2. Initialize git repository: git init**

```sh
git init
```

don't forget to create .gitingore + do initial commit!

> ## **3. Add changes from Working Directory to Index: git add**

![git workspaces](src\git_workspaces.png)

- ### Basic operations:

*add changed file to Index:*

```sh
git add  <file_name>
```

*add all changes from current Working Directory:*

```sh
git add .
```

*remove changes from Index:*

```sh
git reset HEAD <file_name>
```

or

```sh
git restore --staged <file_name>
```

- ### Usefull flags:

*add all changes from project source:*

```sh
git add -A
```

*add just choosen changes from file:*

```sh
git add -p <file_name>
```

> ## **4. Add changes from Index to Repository: git commit**

- commit all changes form Index to Repository:

```sh
git commit -m <commit_message>
```

- commit all changes from Workong Directory to Repository (only if files are already been in Index!):

```sh
git commit -a
```

- commit change/changes from Workong Directory to Repository (only if files are already been in Index!):

```sh
 git commit -m <commit_message> <file(s)_path>
 ```

> ## **5. Usefull commands to show information**
- **Show Working Directory and Index status:**

```sh
git status
```

*show commit information:*

```sh
git show <commit_tag> --pretty=fuller
```

- **Show commits history:**
- commits history
```sh
git log
```
- short version of commits history
```sh
git log --oneline 
```
- branches graph
```sh
git log --graph
```


> ## **6. Checkout to another commit or branch: git checkout**
```sh
git checkout <branch_name>/<commit_tag>
```

> ## **7. Branches**
- create new branch
```sh
git branch <branch_name>
```
- create and checkout to new branch
```sh
git checkout -b <branch_name>
```
- merge branches
```sh
git checkout <destination_branch_name>
git merge <branch_to_merge_name>
```
- delete branch
```sh
git branch -d <branch_name>
```