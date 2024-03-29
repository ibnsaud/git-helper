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

- add just given change/changes to Index:

```sh
git add  <file_name>
```

- add all changes from current Working Directory:

```sh
git add .
```

- add all changeg from project source:

```sh
git add -A
```

- show commit information:

```sh
git show <commit_tag> --pretty=fuller
```

- add just choosen changes/change form file:

```sh
git add -p <file_name>
```

- remove changes from Index:

```sh
git reset HEAD <file_name>
```

- remove dir from Index, but still in Working Directory:

```sh
git rm -r --cashed <dir_name>
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
 git commit -m <commit_message> <file(s) path>
 ```

> ## **5. Usefull commands to show information**
- **Show Working Directory and Index status:**

```sh
git status
```

- **Show commits history:**

```sh
git log
```

> ## **6. Chekcout to another commit or branch: git checkout**
```sh
git checkout <branch_name>/<commit_tag>
```