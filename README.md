git filter-repo --path .env --invert-paths
echo ".env" > .gitignore
git add .gitignore
echo "API_KEY=your_api_key_here" > .env.example
echo "DB_PASSWORD=your_db_password_here" >> .env.example
git add .env.example
git commit -m "Remove .env from history, add .gitignore and .env.example"
git remote add origin https://github.com/YOURUSERNAME/git-security-fix.git
git push origin main --force
