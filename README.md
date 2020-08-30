# TestKitchen
Playing around with test kitchen

## pip3 is required
```
sudo apt install python3-pip
```
## pyenv is required for this repo
### If pyenv is not setup:
```
git clone https://github.com/tfutils/tfenv.git ~/.tfenv
```
### Add bin files to PATH
```
echo 'export PATH="$HOME/.tfenv/bin:$PATH"' >> ~/< .zshrc|.bashrc >
```
### Or symlink bin files to /usr/local/bin
```
ln -s ~/.tfenv/bin/* /usr/local/bin/
```
### Then setup a virtualenv
```
pyenv install 3.8.5
pyenv virtualenv 3.8.5 ansible
pyenv local ansible
```

## tfenv is required for this repo
### If tfenv is not setup:
```
git clone https://github.com/tfutils/tfenv.git ~/.tfenv
```
### Add bin files to PATH
```
echo 'export PATH="$HOME/.tfenv/bin:$PATH"' >> ~/< .zshrc|.bashrc >
```
### Or symlink bin files to /usr/local/bin
```
ln -s ~/.tfenv/bin/* /usr/local/bin/
```

## rbenv is required for this repo
### If rbenv is not setup:
```
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
```
### Add bin files to PATH
```
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/< .zshrc|.bashrc >
```
### Or symlink bin files to /usr/local/bin
```
ln -s ~/.rbenv/bin/* /usr/local/bin/
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