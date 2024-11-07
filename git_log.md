# `git log`

The `git log` command is a fundamental tool in Git that allows you to explore the history of commits in a repository. It provides a detailed view of the changes made to the codebase over time, including who made the changes, when, and what the changes entailed.

## So, let's see how to use it with some examples

In your console, after navigating to your repository folder, run the following:

```bash
  git log
```

and the output will be:

![image](https://github.com/user-attachments/assets/976c72d0-4ba0-41d0-b775-660377377239)

By default, `git log` presents a comprehensive output for each commit, encompassing:

* **Commit hash:** A unique identifier for the commit.
* **Author:** The individual who made the commit.
* **Date:** The timestamp of the commit.
* **Commit message:** A brief description of the changes introduced by the commit.

> [!NOTE]
> In addition to the default output, `git log` offers a variety of options to customize the information displayed and filter the commits shown. This flexibility makes it a powerful tool for navigating and understanding the commit history of any Git repository.

## More examples!

```bash
  git log --pretty=oneline
```

This command gives you a compact view of your Git commit history. It displays each commit on a single line, showing the commit's unique ID (hash) and its message. This is useful for quickly scanning through your project's history and getting a general idea of the changes that have been made over time.

output:

![image](https://github.com/user-attachments/assets/d0d4715f-d173-4560-a941-9fb6b46b35ad)

```bash
  git log --since=5.weeks --pretty=oneline
```

In this case, we add a filter to the git log command to show only commits from the last 5 weeks. This command displays the history of commits made in your Git repository within that time frame.

![image](https://github.com/user-attachments/assets/0f8020e3-8077-4fd4-919b-b00d6c9f33ef)


## And there is more!

Here are some of the most common modifiers for the `git log` command:

```bash 
git log --oneline
```
We already test ir above!

```bash 
git log -p
```
Displays the changes introduced by each commit (the "patch"). Useful for understanding the details of code modifications.

```
bash git log --stat
```
Shows statistics for each commit, including the files modified and the number of lines added/deleted. Provides a summary of the impact of each commit.

![image](https://github.com/user-attachments/assets/03b92489-feb9-454f-8627-322feb6f5c2c)

```bash 
git log --author="Leandro Rey"
```
Filters the commits to show only those made by a specific author. You can use the author's name or email.

```bash 
git log --since="2 weeks ago"
```
Shows only commits made after a specific date. 

```bash 
git log --until="2023-12-31"
```
Shows only commits made before a specific date.

```bash 
git log --grep="Update metadata"
```
Filters the commits to show only those with commit messages that match the given pattern.

![image](https://github.com/user-attachments/assets/4c3a8068-c013-49d5-a3f4-8de10ef84e4d)

```bash 
git log -n 10
```
Limits the output to a specific number of commits. This example shows the last 10 commits.

> [!TIP]
> You can combine these modifiers for more specific filtering and formatting.

## Combining Modifiers

As you already know, you can combine these modifiers for more specific filtering and formatting. 

For example, to see the last 5 commits made by me within the past 15 weeks in a concise one-line format:

```bash
    git log --since=15.weeks --pretty=oneline -n 5 --author="Leandro Rey"
```

output:

![image](https://github.com/user-attachments/assets/f9b4653d-a095-4af3-a38a-b7f02d55dea0)

