git status
git checkout -b deepthi-ratatouille
git branch
git add recipes/deepthi-ratatouille.md
git commit -m "Add ratatouille branch"
git push origin deepthi-ratatouille
git checkout -b deepthi-variations
nano recipes/deepthi-ratatouille.md
git stash
git checkout -b deepthi-typo-fix
nano Exercise1/recipes/mentor-classic-carbonara.md
git add Exercise1/recipes/mentor-classic-carbonara.md
git commit -m "Fix 'spageti' typo in carbonara recipe description"
git push origin deepthi-typo-fix
git commit --amend
git checkout deepthi-variations
git stash pop
git add .
git commit -m "Add variations to recipe"
git push origin deepthi-variations
