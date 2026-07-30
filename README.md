name: generate animation

on:
  # run automatically every 24 hours
  schedule:
    - cron: "0 */24 * * *"
  
  # allows to manually run the job at any time
  workflow_dispatch:
  
  # run on every push on the master/main branch
  push:
    branches:
    - master
    - main

jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      # generates a snake game from a github user (<github_user_name>) contributions graph, output a svg animation at <svg_out_path>
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          
      # push the content of <build_dir> to aBerikut adalah template `README.md` yang disempurnakan. Tampilannya dibuat lebih modern, rapi, responsif, serta sudah dilengkapi **fitur animasi Ular (Snake Game)** dari aktivitas kontribusi GitHub kamu.

---

### 📝 Salin Kode Markdown di Bawah Ini:

```markdown
<div align="center">

  <!-- Header Banner / Typing Animation -->
  <h1>Hi 👋, I'm <a href="[https://github.com/FAJRI2378](https://github.com/FAJRI2378)">Arman Tri Fajri</a></h1>
  <h3>Full-Stack & Front-End Web Developer from Jakarta, Indonesia</h3>

  <p>
    <a href="[https://instagram.com/armntrifjri](https://instagram.com/armntrifjri)"><img src="[https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)" alt="Instagram" /></a>
    <a href="[https://www.linkedin.com/in/arman-tri-fajri-2846a7334](https://www.linkedin.com/in/arman-tri-fajri-2846a7334)"><img src="[https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)" alt="LinkedIn" /></a>
    <a href="mailto:armanfajri008@gmail.com"><img src="[https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)" alt="Email" /></a>
  </p>

  <p>
    🎓 Student at <b>SMK Negeri 21 Jakarta</b> & <b>Politeknik Negeri Jakarta</b><br>
    🚀 Currently mastering <b>Laravel, Next.js, and Modern Web Architecture</b>
  </p>

</div>

<hr />

## 🛠️ Tech Stack & Tools

<p align="center">
  <b>Languages & Frameworks</b><br>
  <img src="[https://skillicons.dev/icons?i=php,laravel,js,ts,react,next,tailwind,html,css,c,cpp](https://skillicons.dev/icons?i=php,laravel,js,ts,react,next,tailwind,html,css,c,cpp)" alt="Tech Stack" />
</p>

<p align="center">
  <b>Backend, Database & Hosting</b><br>
  <img src="[https://skillicons.dev/icons?i=nodejs,express,mysql,postgres,mongodb,vercel](https://skillicons.dev/icons?i=nodejs,express,mysql,postgres,mongodb,vercel)" alt="Backend & Cloud" />
</p>

<p align="center">
  <b>Design & Workflow</b><br>
  <img src="[https://skillicons.dev/icons?i=ps,pr,figma,github](https://skillicons.dev/icons?i=ps,pr,figma,github)" alt="Design Tools" />
</p>

<hr />

## 🐍 GitHub Contribution Snake

<p align="center">
  <img src="[https://raw.githubusercontent.com/FAJRI2378/FAJRI2378/output/github-contribution-grid-snake.svg](https://raw.githubusercontent.com/FAJRI2378/FAJRI2378/output/github-contribution-grid-snake.svg)" alt="Snake animation" />
</p>

<hr />

## 📊 GitHub Analytics

<div align="center">

  <img height="185" src="[https://github-readme-stats.vercel.app/api?username=FAJRI2378&show_icons=true&theme=tokyonight&hide_border=true&count_private=true](https://github-readme-stats.vercel.app/api?username=FAJRI2378&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)" alt="Arman's GitHub Stats" />
  <img height="185" src="[https://github-readme-stats.vercel.app/api/top-langs/?username=FAJRI2378&layout=compact&theme=tokyonight&hide_border=true](https://github-readme-stats.vercel.app/api/top-langs/?username=FAJRI2378&layout=compact&theme=tokyonight&hide_border=true)" alt="Top Languages" />

  <br><br>

  <img src="[https://nirzak-streak-stats.vercel.app/?user=FAJRI2378&theme=tokyonight&hide_border=true](https://nirzak-streak-stats.vercel.app/?user=FAJRI2378&theme=tokyonight&hide_border=true)" alt="GitHub Streak" />

</div>

<hr />

## 🏆 GitHub Trophies

<div align="center">
  <img src="[https://github-profile-trophy.vercel.app/?username=FAJRI2378&theme=tokyonight&no-frame=true&margin-w=4](https://github-profile-trophy.vercel.app/?username=FAJRI2378&theme=tokyonight&no-frame=true&margin-w=4)" alt="Trophies" />
</div>

<hr />

<div align="center">

  ### 👁️ Profile Views
  ![Visitor Count](https://visitcount.itsvg.in/api?id=FAJRI2378&icon=5&color=6)

</div>
