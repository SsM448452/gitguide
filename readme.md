# Git Guide
### 1. Config user
```
git config --global user.name "Your Full Name"
git config --global user.email "your-email-address"
git config --list
```

### 2. Init git
```
mkdir "Repository Name"
cd ".\Repository Name"
git init
dir -hidden
```

### 3. First Commit
```  
git status
git add .\file.ext
git status
git commit -m "Commit message: brief description"
git status
```


### 4. Create branch 
```
git branch dir/branch-name
git branch 
```

### 5. Checkout branch  
```
git checkout dir/branch-name
git status
```

### 6. Check your file:  
```
git checkout master
git status
git merge dir/branch-name
git status
```

### 7. Create Stash  
```
git status
git stash
git status
```

### 8. Apply Stash  
```
git stash list
git stash apply
git status
```

### 9. Drop Stash  
```
git stash list
git stash drop 1
git stash list
```

### 10. Pop Stash  
```
git stash list
git stash pop
git stash list
```

### 11. Revert Commit
```
Revert Commit  
git log --oneline
git revert [COMMIT_ID]
```

### 12.Cherry Pick  
```
git log --oneline
git cherry-pick [COMMIT_ID]
```

### 13.Reset  
```
git log --oneline
git reset --soft HEAD~1
(git reset --mixed HEAD~1, Resetea el indice pero no el directorio de trabajo)
(git reset --hard HEAD~1, Resetea el indice y el directorio de trabajo)
(git reset --merge HEAD~1, Resetea el indice y actualiza los archivos en el arbol de trabajo que son diferentes entre HEAD y el commit dado, pero mantiene los demas sin tocar.)
```

### 14.Create Patch  
```
git diff HEAD > <file>
(git format-patch -1 HEAD, Crea un archivo patch para uno o mas commits)
(git format-patch <start_commit>..<end_commit>, Esto generara un archivo patch en el directorio actual para el ultimo commit. Tambien puedes especificar un rango de commits, ejemplo: git format-patch abc123..def456)
```

### 15.Apply Patch  
```
git apply <file>
```

### 16.Init GitHub  
```
git remote add origin [REMOTE-URL]
git push -u origin master
git push origin --all
```