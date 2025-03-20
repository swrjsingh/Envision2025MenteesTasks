commands for task 9:

git checkout -b rohith-p-variations
git stash save "Added variations"
git checkout main
git checkout -b rohith-typo-fix
git stash pop
git add ..
git commit -m "Fix 'larg' typo in carbonara recipe"
git push origin main
git checkout main
git branch -d rohith-p-variations
