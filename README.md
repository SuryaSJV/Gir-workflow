                               TASK 4

          Build a Version-Controlled DevOps Project with Git

This repository demonstrates a standard Git workflow using branches (`main`, `dev`, `feature`), Git best practices, and proper version control management.

📂 Branch Strategy

- `main` - Stable production branch.
- `dev` - Development/testing branch.
- `feature` - For creating and testing new features before 
              merging into `dev`.


Step 1: Initialize Local Repository and Connect to GitHub
```bash
git init
git remote add origin https://github.com/SuryaSJV/Gir-workflow.git
git branch -M main
```

Step 2: Create First File and Push to "main"
```
echo "This is my first file." > file1.txt
git add .
git commit -m "created file1.txt"
git push -u origin main
```

Step 3: Create "dev" Branch and Add Another File
```
git checkout -b dev
echo "this is my second file." > file2.txt
git add .
git commit -m "created file2.txt"
git push -u origin dev
```

Step 4: Merge "dev" into "main"
```
git checkout main
git pull origin main
git merge dev
git push origin main
```

Step 5: Create feature Branch from dev and Add File
```
git checkout dev
git checkout -b feature
echo "this is my third file." > file3.txt
git add .
git commit -m "created file3.txt"
git push -u origin feature
```

Step 6: Merge "feature" → "dev", Then "dev" → "main"

   Merge feature into dev
```
git checkout dev
git merge feature
git push origin dev
```

   Merge dev into main
```
git checkout main
git merge dev
git push origin main
```


7. Achieved .gitignore and tagging 
```
git tag -a v1.0 -m "Initial release with features, .gitignore, and documentation"

git push origin v1.0
```

![alt text](<Screenshot 2025-04-11 153451.png>)

✅ Final Files in Repository
```
file1.txt → from main
file2.txt → added in dev
file3.txt → added in feature
.gitigone → added files those are not usually in github repository
README.md →  explaining the whole project and work flow
```




