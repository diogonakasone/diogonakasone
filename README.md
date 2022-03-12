### Olá, Eu sou o Combo! 💻

[![Suricato](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/srcq9ffR24)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/vrp.combo/)
[![Twitch](https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white)](https://www.twitch.tv/combofnt)

## Status:

<div align="center">
  <a href="https://github.com/combo0001">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=combo0001&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=combo0001&layout=compact&langs_count=7&theme=dracula"/>
</div>
  
## Tecnologias:
  
<br />

## Ferramentas e Frameworks:

<table style="overflow:hidden">
  <tr>
    <td align="center" width="96">
      <a href="#javascript">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/1200px-Unofficial_JavaScript_logo_2.svg.png" width="48" height="48" alt="JavaScript" />
      </a>
      <br>JavaScript
    </td>
    <td align="center" width="96">
      <a href="#nodejs">
        <img src="https://thidu.dev/images/Nodejs.svg" width="48" height="48" alt="NodeJS" />
      </a>
      <br>NodeJS
    </td>
    <td align="center" width="96">
      <a href="#lua">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Lua-Logo.svg/1200px-Lua-Logo.svg.png" width="48" height="48" alt="Lua" />
      </a>
      <br>Lua
    </td>
    <td align="center" width="96">
      <a href="#html">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/1200px-HTML5_logo_and_wordmark.svg.png" width="48" height="48" alt="HTML" />
      </a>
      <br>HTML
    </td>
    <td align="center" width="96">
      <a href="#css">
        <img src="https://llumine.com.br/wp-content/uploads/2018/03/css-logo-300x300.png" width="48" height="48" alt="CSS" />
      </a>
      <br>CSS
    </td>
  </tr>
</table>

<br />

![Snake animation](https://github.com/combo0001/combo0001/blob/output/github-contribution-grid-snake.svg)

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
          github_user_name: combo0001
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
