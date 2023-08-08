name: Python Deployment

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ec2-user

    steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Set up Python
      uses: actions/setup-python@v2
      with:
        python-version: 3.x

    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt

    - name: Deploy Hello World Python app
      run: python main.py
