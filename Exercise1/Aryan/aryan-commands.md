# Commands

git checkout -b aryan-variations
git stash save "Add variations"
git checkout main
git pull
git checkout -b aryan-typo-fix
git add .
git status
git commit -m "Fix cheese typo in carbonara recipe"
git push origin aryan-typo-fix
git checkout aryan-variations
git stash pop
git add .
git status
git commit -m "Add variations to the recipe"
git push aryan-variation