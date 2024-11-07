# `git init`

The `git init` command is the fundamental command to set up your repository. In many cases, this command is executed automatically when you create a repo using any service or tool.

For example here, in github, when you create a new repo and select:

![image](https://github.com/user-attachments/assets/28404b24-bdcd-4082-a249-d2428dcd4098)

GitHub will execute `git init` for you and automatically create a default README.md file.

## How to initialize a Git repository manually

If you want to initialize a Git repository manually, you need to follow these steps:

 Create a new folder for your project (the command may vary depending on your operating system).
```bash
mkdir NewRepo
```

Go inside your project folder.
```bash
cd NewRepo
```

Run the command to initialize a Git repository.
```bash
git init -> 
```

![image](https://github.com/user-attachments/assets/269a4557-ed82-4aac-acbe-1470eda1fadd)

## So...what does this command do, exactly?
```bash
  git init
```

When you run this command, it creates a hidden directory named `.git` within your project's root directory. This directory is the core of your Git repository and stores all the necessary metadata and history for version control. 

![image](https://github.com/user-attachments/assets/36520a9c-7034-4410-8420-d56671fef635)

Inside this folder you can find:

* Objects database: Stores the different versions of your files (blobs), directories (trees), and commits.
* Index: Also known as the staging area, it acts as a buffer zone where you prepare changes before committing them.
* HEAD: A pointer that references the currently checked-out branch or commit.
* Configuration files: Files to store repository-specific settings and user information.
* Branches: By default, a main branch is created, representing the main line of development.

> [!NOTE]
> Running git init in an existing repository is safe. Git is smart enough to realize that the folder is already a repository. It won't delete anything or mess up your existing Git history.

## Why would you ever run `git init` again?

> [!TIP]
> * **New templates:** Git uses templates to create certain files automatically (like the initial commit message). If you've added new templates to your system, running git init again will make sure your repository uses them.
>   
> * **Moving the repository:** If you want to move your repository to a different location on your computer, you can use the --separate-git-dir option with git init. This lets you keep the repository's data in one place and the actual project files in another.

## More information
* https://git-scm.com/docs/git-init
