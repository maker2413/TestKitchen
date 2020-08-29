# TestKitchen
Playing around with test kitchen

## pyenv is required for this repo
### If pyenv is not setup:
```
pyenv install 3.8.5
pyenv virtualenv 3.8.5 ansible
pyenv local ansible
```

### If the virtualenv is correctly activated:
`python --version` should return 3.8.5

```
pip install -r requirements.txt
```

## awscli is also required for this repo
### If awscli is not setup:
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
rm -rf ./aws
rm awscliv2.zip
```

You will also need you AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, and AWS_DEFAULT_REGION in your .bashrc or .zshrc