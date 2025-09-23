## Hi there 👋  
I'm __Mohamad__, a passionate developer who loves coding, learning, and building cool stuff 🚀  
- 🌱 Currently learning: Python 
- 📫 How to reach me: `mohamadshakiba09@gmail.com` or Linkdin : `www.linkedin.com/in/mohamadshakiba`

✨ "Code, Coffee, Repeat." ☕💻

🚀 "Always learning, always building."

🧩 "Turning ideas into reality, one commit at a time."

🎯 "Focus on progress, not perfection."

🌍 "Sharing knowledge through open source."

😎 "Keep it simple, keep it clean."


![Your GitHub stats](https://github-readme-stats.vercel.app/api?username=mohamadshakibaa&show_icons=true&theme=radical)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=mohamadshakibaa&layout=compact&theme=radical)

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white) 
![Git](https://img.shields.io/badge/-Git-F05032?logo=git&logoColor=white)

name: generate pacman game

on:
  schedule:
    - cron: "0 0 * * *"      # روزی یک‌بار
  workflow_dispatch:         # اجرا دستی از تب Actions
  push:
    branches: [ main ]

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    steps:
      - name: Generate pacman-contribution-graph.svg
        uses: abozanona/pacman-contribution-graph@main
        with:
          github_user_name: mohamadshakibaa

      - name: Publish to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

## My Contribution Graph (Pac-Man)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mohamadshakibaa/mohamadshakibaa/output/pacman-contribution-graph-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mohamadshakibaa/mohamadshakibaa/output/pacman-contribution-graph.svg" />
  <img alt="Pac-Man contribution graph" src="https://raw.githubusercontent.com/mohamadshakibaa/mohamadshakibaa/output/pacman-contribution-graph.svg" />
</picture>
