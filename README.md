# TestKitchen
Playing around with test kitchen

## pip3 is required
```
sudo apt install python3-pip
```

## pyenv is required for this repo
### If pyenv is not setup:
```
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```
### Add bin files to PATH
```
echo 'export PATH="$HOME/.pyenv/bin:$PATH"' >> ~/< .zshrc|.bashrc >
```
### Or symlink bin files to /usr/local/bin
```
ln -s ~/.pyenv/bin/* /usr/local/bin/
```
### Add the following to your .zshrc or .bashrc
```
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
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
### Add the following to your .zshrc or .bashrc
```
eval "$(rbenv init -)"
```
### Install ruby-build
```
mkdir -p "$(rbenv root)"/plugins
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
```

## Setup Virtual environments
### Virtualenv:
```
pyenv install 3.8.5
pyenv virtualenv 3.8.5 ansible
pyenv local ansible
```
If the virtualenv is correctly activated:
`python --version` should return 3.8.5
```
pip install -r requirements.txt
```
### Terraform:
```
tfenv install 0.13.2
tfenv use 0.13.2
```
### Ruby:
```
rbenv install 2.7.1
rbenv local 2.7.1
rbenv rehash
```

## Install bundler
```
gem install bundler
```

## Install TestKitchen and plugins
```
bundle install
```
This command will install the bundle specified in `Gemfile`
### Initialize TestKitchen
```
kitchen init
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