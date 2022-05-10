# gitartwork on user's contribution graph

gitartwork on user's contribution graph, make a SVG image of it and finally push it back to your repository.

An example result:
[![jasineri/gitartwork](gitartwork.svg)](https://github.com/jasineri/gitartwork)

## Usage:

### Option #1: Use gitartwork as a GitHub Action
1. Copy the workflow code into a `.github/workflows/gitartwork.yml` file in your repository.

        name: gitartwork from a contribution graph
        on: 
          push:
          schedule:
            - cron: '* */24 * * *'
        jobs:
          build:
            name: Make gitartwork SVG
            runs-on: ubuntu-latest
            steps:
              - uses: actions/checkout@v3
              - uses: jasineri/gitartwork@v1
                with:
                   # Use this username's contribution graph  
                   user_name: jasineri
                   # Text on contribution graph 
                   text: JASINERI
              - uses: jasineri/simple-push-action@v1

2. A few moments later it will generate `gitartwork.svg` image in your repository, so then you can include it in your `README.md` like `![gitartwork](gitartwork.svg)`
3. Have fun :)

### Option #2: Make gitartwork locally on your environment
Still in progress...
