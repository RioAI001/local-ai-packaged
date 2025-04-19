# To copy (clone) a GitHub repository so that your copy remains linked and you can pull/apply future updates from the original, you should **fork** the repository and then configure your local copy to track both your fork and the original ("upstream") repository.

## Step-by-Step Instructions

** 1. Fork the Repository on GitHub**

- Go to the original repository page on GitHub.
- Click the **Fork** button in the top right corner. This creates a copy of the repository under your GitHub account[1][5][8].

** 2. Clone Your Fork Locally**

- On your forked repository page, click the **Code** button and copy the URL.
- In your terminal, run:

  ```bash
  git clone https://github.com/YOUR-USERNAME/REPO-NAME.git
  ```

  This creates a local copy of your fork[1][5].

** 3. Add the Original Repository as an "Upstream" Remote**

- Change directory into your cloned repo:

```bash
cd REPO-NAME
```

- Add the upstream remote:

```bash
git remote add upstream https://github.com/ORIGINAL-OWNER/ORIGINAL-REPO.git
```

- Verify remotes:

```bash
git remote -v
```

You should see `origin` (your fork) and `upstream` (the original)[1][2].

** 4. Keeping Your Fork Synced**

- To fetch and merge changes from the original repo:

```bash
git fetch upstream
git checkout main
git merge upstream/main
```

- Then push to your fork if needed:

```bash
git push origin main
```

  This workflow keeps your fork and local copy updated with the latest changes from the original repository[1][2][4].

## Summary Table

| Action                | Command/Step                                                                 |
|-----------------------|------------------------------------------------------------------------------|
| Fork on GitHub        | Click "Fork" on the original repo page                                       |
| Clone your fork       | `git clone https://github.com/YOUR-USERNAME/REPO-NAME.git`                   |
| Add upstream remote   | `git remote add upstream https://github.com/ORIGINAL-OWNER/ORIGINAL-REPO.git`|
| Fetch upstream changes| `git fetch upstream`                                                          |
| Merge changes         | `git merge upstream/main`                                                     |
| Push to your fork     | `git push origin main`                                                        |

This setup ensures your copy is linked and you can always pull and apply future updates from the original repository[1][2][4].

Citations:
[1] https://docs.github.com/articles/fork-a-repo
[2] https://docs.github.com/articles/working-with-forks
[3] https://www.youtube.com/watch?v=h8suY-Osn8Q
[4] https://www.freecodecamp.org/news/how-to-fork-a-github-repository/
[5] https://www.geeksforgeeks.org/how-to-fork-a-github-repository/
[6] https://docs.github.com/en/desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop
[7] https://www.youtube.com/watch?v=XvxWFST1i4A
[8] https://www.git-tower.com/learn/git/faq/github-fork-repository

---
