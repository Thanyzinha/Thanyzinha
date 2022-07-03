✌🏻Olá! Eu sou a Thanyzinha "Nathany"✌🏻

- 🍀Estudante de TSI📚
- 🍀 Estudando HTML e CSS 💻
- 📫 Contate-me no email: nathanyeleuterio99@gmail.com ou nathany.eleuterio@estudante.ifgoiano.edu.br

##

<div align="center">
  <a href="https://github.com/rafaballerini">
  <a href="https://github.com/Thanyzinha/Thanyzinha">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Thanyzinha&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Thanyzinha&layout=compact&langs_count=7&theme=dracula"/>
</div>
<div style="display: inline_block"><br>
  <img align="center" alt="Rafa-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="Rafa-Ts" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg">
  <img align="center" alt="Rafa-React" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg">
  <img align="center" alt="Rafa-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Rafa-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Rafa-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <img align="center" alt="Rafa-Csharp" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg">
  <img align="right" alt="Rafa-pic" height="150" style="border-radius:50px;" src="https://media.discordapp.net/attachments/639956127056134178/890373478988013628/Publicacoes_Instagram_1_1.png?width=676&height=676">
</div>
 
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: manoguinas
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
