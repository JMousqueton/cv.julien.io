
# Curriculum Vitae for Julien Mousqueton

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-yellow.svg)](https://github.com/JMousqueton/cv.julien.io/blob/main/LICENSE)
[![Twitter: JMousqueton](https://img.shields.io/twitter/follow/JMousqueton.svg?style=social)](https://twitter.com/JMousqueton)

>  Source to build my CV 

## CV  

🌍 https://cv.julien.io


## Documentation

🇫🇷 La [documentation](https://julien.io/Heberger-son-CV-sur-Github) se trouve sur mon blog 

🇺🇸 Quick & Dirty documentation 

Build with Hugo using a modified version of Toha theme 

Github-action : 

```
name: github pages

on:
  push:
    branches:
      - main  # Set a branch to deploy
  pull_request:

jobs:
  deploy:
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v2
        with:
          submodules: true  
          fetch-depth: 0    

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: 'latest'
          # extended: true

      - name: Build
        run: hugo --minify --enableGitInfo 

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        if: github.ref == 'refs/heads/main'
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
```


| Branch | Desc. |
|---|---|
| main | Source code |
| gh-pages | website publish by Github pages |

## Features

- Multilingual 🇫🇷 🇺🇸 

## License

[Apache 2.0](https://github.com/JMousqueton/cv.julien.io/blob/main/LICENSE)


## Author

- [@JMousqueton](https://www.github.com/JMousqueton)

