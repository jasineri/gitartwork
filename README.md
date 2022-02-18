# Gitartwork on user's contribution graph

Gitartwork on user's contribution graph, make a SVG image of it and finally push it back to your repository.

An example result:
[![jasineri/gitartwork](gitartwork.svg)](https://github.com/jasineri/gitartwork)

## Usage:

### Option #1: Include as a GitHub Action
Copy the workflow code into a `.github/workflows/gitartwork.yml` file in your action's repository.

    name: Gitartwork from a contribution graph
    on: [push, pull_request]
    
    jobs:
      build:
        name: Make Gitartwork SVG
        runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v2
          - uses: partinis/gitpaint@v1
            with:
               user_name: jasineri
               text: JASINERI
               svg_file_name: gitartwork.svg

### Option #2: Make locally on your environment
Still in progress...