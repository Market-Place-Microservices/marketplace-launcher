### Steps to Create Git Submodules

1. 🚀 Create a new repository on GitHub.
2. 🖥️ Clone the repository to your local machine.
3. ➕ Add the submodule, where `repository_url` is the repository URL, and `directory_name` is the name of the folder where you want the submodule to be stored (it should not already exist in the project).

   ```bash
       git submodule add <repository_url> <directory_name>
   ```

## ✅Add the changes to the repository (git add, git commit, git push).

```
    * git add .
    * git commit -m "Add submodule"
    * git push
```

🔄 Initialize and update submodules.
When someone clones the repository for the first time, they should execute the following command to initialize and update the submodules.

```
    git submodule update --init --recursive
```

🔃 To update submodule references.

```
     git submodule update --remote
```

## Important

If you're working in the repository that contains the submodules, first update and push in the submodule and then in the main repository.

If done in reverse, submodule references in the main repository will be lost, and conflicts will need to be resolved.
