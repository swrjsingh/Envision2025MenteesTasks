# Recipe Book Challenge
### IEEE Pixel Flow Exercise 1

Welcome to the Recipe Book Challenge! In this exercise, you'll learn Git and GitHub by contributing to a collaborative recipe book. Each task will teach you essential Git concepts while building something fun together.

---

## General Rules
- Name your branches: `yourname-feature` (like `johndoe-italian`)
- Name your recipes: `yourname-recipe-name.md` (like `johndoe-carbonara.md`)
- Stuck? Check out the Hints file - it's super detailed! The Hints file contains all the commands you will need to complete every subtask in every task! But type them out yourself, do not copy-paste! 
- You are free to use Google, ChatGPT and other AI tools for all sorts of help - But finally type the Git commands YOURSELF in the terminal - that's how you'll learn. DO NOT copy-paste commands into the terminal. 
- Questions? We're here to help - feel free to contact us anytime : )
- Finally, make sure you understand every command that you are using. We're assuming you have completed the resources we sent : )
- Ideally, check the hints file for every task (even if you're done with it)
---

## Tasks

### Task 1: Your First Branch and Pull Request
1. Clone this repository to your computer
2. Create a new branch with your name and cuisine type:
   ```
   Example: If your name is John Doe and you're adding an Italian recipe:
   Branch name should be: johndoe-italian
   ```
3. Create a new recipe file in the `recipes` folder:
   ```
   Example: If you're adding a carbonara recipe:
   File name should be: johndoe-carbonara.md
   ```
4. Copy the contents of `recipe-template.md` into your new file and fill in your recipe details
5. Save your changes and create a commit with the message: "Add [recipe name] recipe"
6. Push your branch to GitHub and create a pull request:
   - Title: "New Recipe: [Your Name]'s [Recipe Name]"
   - Description: Briefly describe your recipe and what makes it special

---

### Task 2: Working with .gitignore
1. Create a text file with your secret recipe:
   ```
   File name: yourname-secret-recipe.txt
   Example: johndoe-secret-recipe.txt
   ```
2. Write your secret recipe or any private notes in this file
3. Open the `.gitignore` file and add your secret file name on a new line
4. Create a commit with the message: "Update gitignore to protect secret recipe"
5. Verify your secret file is not being tracked (it should not appear in git status)

---


### Task 3: Resolving Conflicts
1. Update your main branch:
   - Switch to main branch
   - Pull latest changes
2. Create a new branch named `yourname-improvements` (Example: `johndoe-improvements`)
3. Open the file `mentor-classic-carbonara.md` and add two new cooking tips at the bottom of the Tips section:
   ```markdown
   Example additions:
   - Tip: Always reserve some pasta water before draining
   - Tip: Warm the serving bowls before plating
   ```
4. When you try to push, someone else might have changed the same file
5. If you get a conflict:
   - Look for the conflict markers (<<<<<<, =======, >>>>>>>)
   - Keep both your tips and the other person's changes
   - Remove the conflict markers
   - Save and commit with message: "Resolve conflict and add new tips"

---


### Task 4: Git Log and History
1. Use Git's history tools to investigate:
   - Find who last modified `mentor-classic-carbonara.md` and what they changed
   - Find the date and time of the last recipe commit
   - Pick another mentee from your group and list all their commits
   - Look at line 15 in `mentor-classic-carbonara.md` and find who added it
2. Write down your findings in a new file called `yourname-investigation.md`

---


### Task 5: Rebasing and Cleaning History
1. Create a branch named `yourname-formatting` (Example: `johndoe-formatting`)
2. Make these three separate commits to your recipe file:
   ```
   First commit: Add another title and update all titles to use proper markdown (# Recipe Name)
   Second commit: Add blank lines between each section, add horizontal lines with ---
   Third commit: Add bullet points to ingredient list (with - ) if not already done, add another ingredient to the list
   ```
3. Combine these three commits into one commit with the message: "Format recipe file" using git rebase(check hints if needed) 

---


### Task 6: Branch Management
1. By this point, you should have these branches:
   ```
   main (don't delete)
   yourname-cuisine (from Task 1 - should be merged)
   yourname-improvements (from Task 3 - should be merged)
   yourname-formatting (from Task 5 - should be merged)
   ```

2. List all your branches and check which ones are already merged into main using terminal git commands

3. Delete these branches ONLY IF they're merged:
   - `yourname-cuisine` (Task 1 branch)
   - `yourname-improvements` (Task 3 branch)
   - `yourname-formatting` (Task 5 branch)
   
   Note: Only delete branches that are fully merged. If unsure, check with us mentors.


---


### Task 7: Tagging Releases
1. Create a tag for your recipe version:
   ```
   Tag name: v1.0-yourname
   Example: v1.0-johndoe
   ```
2. Add this message to your tag: "First recipe contribution by [Your Name]"
3. Push your tag to the repository

---


### Task 8: Undoing Changes
1. Open your recipe file and make these exact changes:
   ```markdown
   - Change the recipe title to "WRONG RECIPE"
   - Delete the first two ingredients from your list
   - Add this incorrect step: "Microwave for 60 minutes"
   ```
2. Practice undoing these changes using three different methods:
   - Before staging: Undo the title change
   - After staging: Undo the deleted ingredients
   - After committing: Undo the wrong step
   (Ask your mentor for hints if needed)

---


### Task 9: Stashing Changes
1. Create a new branch called `yourname-variations` from your recipe branch
2. Start adding this Variations section to your recipe file:
   ```markdown
   ## Variations
   1. Vegetarian version:
      - Replace pancetta with sautéed mushrooms
      - Add a pinch of smoked paprika for depth
   2. Spicy version:
      - Add red pepper flakes to taste
      - Include one minced garlic clove
   ```
3. Your mentors, Swaraj and Vishruth point out there's a typo in `mentor-classic-carbonara.md` that needs urgent fixing.
   Each mentee has been assigned a specific typo to fix:
   - Aryan: Fix "chese" to "cheese" in Description
   - Deepthi: Fix "spagheti" to "spaghetti" in Ingredients
   - Devansh: Fix "panceta" to "pancetta" in Ingredients
   - Rohit: Fix "larg" to "large" in Ingredients
   - Shubh: Fix "Romani" to "Romano" in Ingredients
   - Rohan: Fix "Regiano" to "Reggiano" in Ingredients

4. Steps to handle this situation:
   - Save your unfinished Variations work using stash (don't commit it yet) (check hints file for this task)
   - Switch to a new branch called `yourname-typo-fix`
   - Fix ONLY your assigned typo in the mentor's recipe
   - Commit and push the fix
   - Create a PR titled "Fix [your assigned word] typo in carbonara recipe"
   - Switch back to your variations branch
   - Recover your saved work
   - Complete and commit your Variations section

5. Create a new file called `yourname-commands.md` with all the git commands you used to complete this task

Note: Only fix your assigned typo. If you notice other typos, do not fix them - they are assigned to other mentees.

---


### Task 10: Final Challenge
1. Create a branch named `yourname-final` (Example: `johndoe-final`)

2. Create a folder with your name in the Exercise1 directory and collect all your .md files:
   ```
   Exercise1/
   ├── yourname/
   │   ├── yourname-investigation.md    (from Task 4)
   │   ├── yourname-branches.md         (from Task 6)
   │   └── yourname-commands.md         (from Task 9)
   ```

3. Create `table-of-contents.md` with this format:
   ```markdown
   # Recipe Book Contents
   
   ## Main Dishes
   - [Carbonara](./recipes/johndoe-carbonara.md) by John Doe
   - [Recipe Name](./path-to-recipe) by Author Name
   ```

4. Add your name to `README.md` under the Contributors section:
   ```markdown
   ## Contributors
   - Your Name - [Your Recipe Name]
   ```

5. Request reviews on GitHub:
   - Go to your pull request
   - Click the gear icon next to "Reviewers" on the right
   - Select both mentor names from the list
   - Add a comment asking for their review

And that's it : )
