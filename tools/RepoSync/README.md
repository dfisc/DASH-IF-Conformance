# Repository Syncing

The script prvided in this directory syncs the [DASH-IF-Conformance repository](https://github.com/Dash-Industry-Forum/DASH-IF-Conformance) to the desired repository.

The steps to be followed are:
1. Each local repository used for committing changes here should have a remote called "downstream" pointing to the desired repository.
```
> git remote add downstream <URL_to_desied_repository>
```

2. Modify the list of submodules allowed to be pushed to the desired location in the script
```
> allowedmodules=("TestSubmoduleNeeded") # List the modules allowed to be pushed
```

3. Modify the local directory path of your desired main repository in the script
```
> desiredlocal="/var/www/html/TestGitSync/Gitlab/Test/"
```

4. Run the script
```
> ./sync.sh
```

5. **Go to your desired main repository and merge the "sync" branch. Delete the "sync" branch after merge.**
