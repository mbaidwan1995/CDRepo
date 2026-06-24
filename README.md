name: CI-CD-Pipeline

on:
  push:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Build Application
        run: echo "Building application..."

  test:
    needs: build
    runs-on: ubuntu-latest

    steps:
      - name: Run Tests
        run: echo "Running tests..."

  deploy:
    needs: test
    runs-on: ubuntu-latest

    steps:
      - name: Deploy Application
        run: echo "Deploying application to production..."
