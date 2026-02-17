<h1 align="center">Hi 👋, I'm Unmesh</h1>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?size=25&duration=4000&color=00F72A&center=true&vCenter=true&width=500&lines=Full+Stack+Developer;Java+%7C+MERN+Stack;Passionate+About+Coding;Always+Learning+New+Things" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=unmesh-patil-mh&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=unmesh-patil-mh&theme=radical&hide_border=true&background=0D1117" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=unmesh-patil-mh&theme=react-dark&bg_color=0D1117&hide_border=true" />
</p>


name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: your-username
          outputs: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
