---
icon: lucide/rocket
---

# Quickly create a markdown project and deploy it to GitHub pages

1. Create the project with python uv  
   `uv init my-project && cd my-project`

2. Generate the site template with Zensical  
   `uv add --dev zensical && uv run zensical new`

3. Commit locally  
   `git add . && git commit -m "init project"`

4. Create the GitHub repository from terminal and push  
   `gh repo create Dronicode/my-project --public --source=. --remote=origin`

5. Enable GitHub Pages to build with GitHub Actions  
   `gh api -X POST repos/Dronicode/my-project/pages -f build_type=workflow`

6. Push to GitHub  
   `git push -u origin main`

7. Enjoy the finished result  
   https://dronicode.github.io/my-project/
