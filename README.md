# gitartwork on user's contribution graph

gitartwork on user's contribution graph, make a SVG image of it and finally push it back to your repository.

An example result:
[![jasineri/gitartwork](gitartwork.svg)](https://github.com/jasineri/gitartwork)

## Usage:

### Option #1: Use gitartwork as a GitHub Action
Copy the workflow code into a `.github/workflows/gitartwork.yml` file in your action's repository.

    name: gitartwork from a contribution graph
    on: 
      schedule:
        - cron: '* */24 * * *'
    workflow_dispatch:
    jobs:
      build:
        name: Make gitartwork SVG
        runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v2
          - uses: jasineri/gitartwork@v1
            with:
               user_name: jasineri
               text: JASINERI
          - uses: jasineri/simple-push-action@v1

### Option #2: Make gitartwork locally on your environment
Still in progress...