# Jae Hwang
![Python](https://img.shields.io/badge/Python-blue.svg?&style=for-the-badge&logo=Python&logoColor=white)
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=khwwang&theme=tokyonight&show_icons=true)
name: Update gist
on:
  push:
    branches:
      - master
  schedule:
    - cron: "0 0 * * *"
jobs:
  update-gist:
    runs-on: ubuntu-latest
    steps:
      - name: Update gist
        uses: maxam2017/productive-box@master
        env:
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
          GIST_ID: ${{ secrets.GIST_ID }}
          TIMEZONE: Asia/Seoul
