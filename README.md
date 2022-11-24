# action-deploy-s3-cloudfront

Publish on S3 and invalidate Cloudfront

## Usage

```yaml

#... run config ...

jobs:
  name-job:
    runs-on: ubuntu-latest
    steps:
      # Add like first step
      - name: Deploy on S3 / Invalidate CloudFront
        uses: Travelonux/action-deploy-s3-cloudfront@main
        with:
          token: ${{ secrets.GITHUB_TOKEN }}

      #... next steps ...     

```

## Configuration

The following inputs are available (some of them are optional):

| Input (click on name for description)                                                                                                     |                      Allowed values                      | Default | Required
|:------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------:|:-------:|:---------:|
| <details><summary>`token`</summary><br/>Github Personal Access Token with permission on repo (or `${{ secrets.GITHUB_TOKEN }}`)</details> | Valid [Github Token](https://github.com/settings/tokens) |    -    |    yes
| <summary>`fetch-depth`</summary>                                                                                                          |   Like [Checkout](https://github.com/actions/checkout)   |    1    |    no
| <summary>`node-version`</summary>                                                                                                          | Like [Setup-Node](https://github.com/actions/setup-node) |    16.x    |    no    


