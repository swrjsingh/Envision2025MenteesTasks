```md

git checkout -b devansh-variation
git stash save "Stashing it for some time"
git checkout main
git pull
git checkout -b devansh-typo-fix
git add .
git commit -m "Typo fixed"
git push devansh-typo-fix
git branch -d devansh-typo-fix
git checkout devansh-variation
git stash pop
git add .
git commit -m "Coming back and saving the Ingredients changes"
git push devansh-variation
git checkout main
git branch -D devansh-variation
```