# action-node-npm-cache

Checkout Code, Setup Node and NPM Cache by SO

## Usage

```yaml

#... run config ...

jobs:
  name-job:
    runs-on: ubuntu-latest
    steps:
      # Add like first step
      - name: Checkout / Setup Node / NPM-Cache
        uses: rodobarcaaa/action-node-npm-cache@main
        with:
          token: ${{ secrets.REPO_GITHUB_TOKEN }}

      #... next steps ...     

```

## Configuration

The following inputs are available (some of them are optional):

| Input (click on name for description)                                                                                                     |                      Allowed values                      | Default | Required
|:------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------:|:-------:|:---------:|
| <details><summary>`token`</summary><br/>Github Personal Access Token with permission on repo (or `${{ secrets.GITHUB_TOKEN }}`)</details> | Valid [Github Token](https://github.com/settings/tokens) |    -    |    yes
| <summary>`fetch-depth`</summary>                                                                                                          |   Like [Checkout](https://github.com/actions/checkout)   |    1    |    no
| <summary>`node-version`</summary>                                                                                                          | Like [Setup-Node](https://github.com/actions/setup-node) |    16.x    |    no    


