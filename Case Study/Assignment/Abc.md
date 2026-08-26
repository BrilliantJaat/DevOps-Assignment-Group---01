# Create project
mkdir student-project
cd student-project

# Initialize Git
git init

# Create README
echo "# Student Project" > README.md

# Check status
git status

# Stage files
git add .

# Commit
git commit -m "Initial project"

# Rename branch
git branch -M main

# Connect GitHub repository
git remote add origin https://github.com/USERNAME/student-project.git

# Upload project
git push -u origin main

# Create a feature branch
git switch -c new-feature

# Make changes, then stage them
git add .

# Commit changes
git commit -m "Added new feature"

# Push branch
git push -u origin new-feature

# Return to main
git switch main

# Merge feature
git merge new-feature

# Push merged changes
git push origin main
