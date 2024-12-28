# Dokploy Deploy Action

This repository contains GitHub Actions for deploying applications with image URI in Dokploy. 

## Features

- Update application with image URI
- Trigger deployment on Dokploy
- Easy integration with GitHub workflows

## Usage

To use these actions in your GitHub workflow, add the following to your `.github/workflows/deploy.yml` file:

```yaml
name: Deploy application

on:
  push:
    branches:
      - main

jobs:
  dokploy_deploy:
    uses: rarg27/dokploy-deploy-action@v1
    with:
      api_token: ${{ secrets.DOKPLOY_API_TOKEN }}
      application_id: ${{ secrets.DOKPLOY_APPLICATION_ID }}
      dokploy_url: ${{ secrets.DOKPLOY_URL }}
      image_uri: 123456789123.dkr.ecr.ap-southeast-1.amazonaws.com/example:latest

```

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any bugs or feature requests.