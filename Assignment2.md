### Patr 1: Dealing with git
1. Describe what is the output of the following commands
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
'git branch' will list your branches
    two branches 'master' and 'math' are in this repo
'git checkout BRANCH_NAME' 
    Can switch to use other branchs
'git log --decorate'
    Will check the last commits and print out the ref names of any commits that are shown
```

2. Try `git log --graph --all`. What do you see?
```
It shows a graphic branch commit history
```

3. Use `git diff BRANCH_NAME` to view the differences from a branch and the current branch.
   Summarize the difference from master to the other branch.

```
git diff math
    'math' branch changed A.py and B.py
    A.py deleted 11 lines and add 3 lines
    B.py added 1 line
```

4. Write a command sequence to merge the non-master branch into `master`

```
git checkout master
git merge math
```


5. Write a command (or sequence) to (i) create a new branch called `math` (from the `master`) 
and (ii) change to this branch (yes, `math` is already there, just report what you've done, the error and the reason you got the error. If you deleted and recreated the branch, you are fine too)

```
git branch -d math
git checkout -b math

```
   
6. Edit B.py adding the following source code below the content you have there
```
print 'I know math, look:'
print 2+2

Done
```

7. Write a command (or sequence) to commit your changes
```
git commit -a -m "B1.py"
```

8. Change back to the `master` branch and change B.py adding the following source code (commit your change to `master`):
```
print 'hello world!'

Done
```

9. Write a command sequence to merge the `math` branch into `master` and describe what happened
```
git checkout master
git merge math

git merge math
Auto-merging B.py
CONFLICT (content): Merge conflict in B.py
Automatic merge failed; fix conflicts and then commit the result
```
   
10. Write a set of commands to abort the merge
```
git reset --hard head

```
   
11. Now repeat item 9, but proceed with the manual merge (Editing B.py). All implemented functions are needed. Explain your procedure
```
I edit B.py by adding
    print 'I know math, look:'
    print 2+2
```

12. Write a command (or set of commands) to proceed with the merge and make `master` branch up-to-date
```
git commit -a -m "B2"
```

### Part 2: Using GitHub

# Nonrigid Structure-from-Motion: Estimating Shape and Motion with Hierarchical Priors

**Member, IEEE, and Christoph Bregler**

_15 pages_

## Out comes:

1.Due to the inevitable presence of measurement noise, missing data and high-dimensional spaces, we argue that NRSFM is best posed as a statistical estimation problem.

2.Extracting 3D shape and motion of nonrigid objects from 2D point track.

3.Estimating time-varying 3D shape from monocular 2D point tracks is inherently underconstrained without prior assumptions.

[link of the paper](https://ieeexplore.ieee.org/document/4359359)



