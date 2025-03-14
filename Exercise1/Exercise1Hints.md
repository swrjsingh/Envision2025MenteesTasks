# Recipe Book Challenge - Hints 🍳

This guide provides hints for each task in the Recipe Book Challenge.

## Task 1: Your First Branch and Pull Request
```bash
# Clone the repository
git clone [repository-url]

# Create and switch to your branch
git checkout -b john-doe-italian

# Create your recipe file in the recipes folder
# Edit the file with your recipe content

# Stage and commit
git add .
git commit -m "📝 Add spaghetti carbonara recipe by John Doe"

# Push and create PR
git push origin john-doe-italian
```

## Task 2: Working with .gitignore
```bash
# Create your secret recipe file
touch secret-ingredients.txt

# Edit .gitignore to add the file
echo "secret-ingredients.txt" >> .gitignore

# Commit the .gitignore change
git add .gitignore
git commit -m "🔒 Update gitignore to protect secret recipe"
```

## Task 3: Resolving Conflicts
```bash
# Update main branch
git checkout main
git pull origin main

# Create improvement branch
git checkout -b john-doe-improvements

# Edit someone's recipe and commit
git add .
git commit -m "✨ Add cooking tips to carbonara recipe"

# If conflict occurs during PR:
git pull origin main
# Resolve conflicts in your editor
git add .
git commit -m "🔄 Resolve merge conflicts"
git push origin john-doe-improvements
```

## Task 4: Git Log and History
```bash
# View commit history
git log

# Check specific author's commits
git log --author="John Doe"

# See changes in specific file
git log -p recipes/jane-doe-lasagna.md

# Find who modified each line
git blame recipes/jane-doe-lasagna.md
```

## Task 5: Rebasing and Cleaning History
Here's a step-by-step guide to complete this task:

1. First, create your formatting branch:
   ```bash
   git checkout main
   git pull origin main
   git checkout -b yourname-formatting
   ```

2. Make your three commits in sequence:
   ```bash
   # First commit - Update titles
   # Edit your recipe file
   git add .
   git commit -m "Update titles to proper markdown format"

   # Second commit - Add spacing
   # Edit your recipe file
   git add .
   git commit -m "Add spacing and horizontal lines"

   # Third commit - Update ingredient list
   # Edit your recipe file
   git add .
   git commit -m "Update ingredient list formatting"
   ```

3. Now, let's combine these commits using interactive rebase:
   ```bash
   # Start interactive rebase for the last 3 commits
   git rebase -i HEAD~3
   ```

4. In the editor that opens, you'll see something like:
   ```
   pick abc1234 Update titles to proper markdown format
   pick def5678 Add spacing and horizontal lines
   pick ghi9012 Update ingredient list formatting
   ```

5. Change it to:
   ```
   pick abc1234 Update titles to proper markdown format
   squash def5678 Add spacing and horizontal lines
   squash ghi9012 Update ingredient list formatting
   ```

6. Save and close the editor. A new editor will open for the combined commit message.
   Replace all text with:
   ```
   Format recipe file
   
   - Update titles to proper markdown
   - Add spacing and horizontal lines
   - Update ingredient list formatting
   ```

7. If anything goes wrong during rebase:
   ```bash
   # To abort the rebase and start over
   git rebase --abort
   
   # Then try again from step 3
   ```

8. Verify your changes:
   ```bash
   # Should show only one commit
   git log -n 1
   
   # Should show all your changes are still there
   git diff origin/main
   ```

9. Push your changes:
   ```bash
   git push origin yourname-formatting --force-with-lease
   ```

IMPORTANT NOTES:
- NEVER use `--force-with-lease` on shared branches like `main`
- Make sure you have committed all changes before rebasing
- If you're unsure, ask your mentor before proceeding
- Take a screenshot of your commits before rebasing (just in case)

## Task 6: Branch Management
Here's how to manage your branches safely:

1. List and check branch status:
   ```bash
   # List all local branches
   git branch

   # List all branches that are merged into main
   git branch --merged main

   # List all branches that are NOT merged into main
   git branch --no-merged main
   ```

2. Before deleting branches:
   ```bash
   # Make sure you're not on the branch you want to delete
   git checkout main

   # Update your local repo with remote changes
   git fetch origin
   git pull origin main
   ```

3. Delete merged branches safely:
   ```bash
   # Safe delete (only if branch is merged)
   git branch -d yourname-cuisine
   git branch -d yourname-improvements
   git branch -d yourname-formatting
   ```

4. If you get an error about unmerged branches:
   ```bash
   # 1. Check if the PR was merged on GitHub
   # 2. Update your local repo
   git fetch origin
   
   # 3. Try deleting again
   git branch -d branchname
   
   # 4. If still getting errors, DO NOT use -D
   #    Ask mentors first!
   ```

5. Create your branch status file:
   ```bash
   # Create and open the file
   touch yourname-branches.md
   
   # Add your branch information following the template
   # Example content:
   # ## Deleted Branches
   # - yourname-cuisine - Merged into main after Task 1
   # - yourname-improvements - Merged after adding cooking tips
   #
   # ## Active Branches
   # - main - Primary branch
   # - yourname-variations - Working on recipe variations
   ```

## Task 7: Tagging Releases
```bash
# Create annotated tag
git tag -a v1.0 -m "First recipe book release"

# Push tag
git push origin --tags
```

## Task 8: Undoing Changes
```bash
# Undo staged changes
git reset HEAD recipe.md

# Undo committed changes (before push)
git reset --soft HEAD^

# Revert pushed changes
git revert abc123def456

# Undo all working directory changes
git reset --hard HEAD
```

## Task 9: Stashing Changes
```bash
# 1. Create and switch to variations branch from your recipe branch
git checkout yourname-recipe    # Switch to your recipe branch first
git checkout -b yourname-variations

# 2. After adding the Variations section (but before committing)

# 3. Save your work in progress
git stash save "WIP: Adding variations section"

# 4. Create typo fix branch from main
git checkout main
git pull origin main
git checkout -b yourname-typo-fix

# Fix your assigned typo in mentor-classic-carbonara.md
# Example for Aryan (each mentee will have different changes):
git add recipes/mentor-classic-carbonara.md
git commit -m "Fix 'chese' typo in carbonara recipe description"
git push origin yourname-typo-fix

# Create PR on GitHub with title: "Fix [your word] typo in carbonara recipe"

# Go back to your variations branch
git checkout yourname-variations

# Bring back your saved work
git stash pop

# After completing variations section
git add .
git commit -m "Add variations to recipe"
git push origin yourname-variations
```

## Task 10: Final Challenge
```bash
# Create your final branch
git checkout -b yourname-final

# Create your personal folder and move your files
mkdir Exercise1/yourname
mv Exercise1/yourname-investigation.md Exercise1/yourname/
mv Exercise1/yourname-branches.md Exercise1/yourname/
mv Exercise1/yourname-commands.md Exercise1/yourname/

# Create table of contents
touch Exercise1/table-of-contents.md
# Edit the file with your content

# Update README.md with your details
# Edit the Contributors section

# Stage all changes
git add Exercise1/yourname/
git add Exercise1/table-of-contents.md
git add README.md

# Commit and push
git commit -m "Complete final challenge"
git push origin yourname-final
```

## Common Issues and Solutions

### If you accidentally committed to main
```bash
# Create new branch with current changes
git checkout -b feature-branch
# Reset main to original state
git checkout main
git reset --hard origin/main
```

### If you need to update your PR branch
```bash
git checkout main
git pull origin main
git checkout your-feature-branch
git rebase main
git push origin your-feature-branch --force
```

### If you need to undo a merge
```bash
git reset --hard HEAD~1
```
