# TestKitchen
Playing around with test kitchen

# If pyenv not setup
pyenv install 3.8.5
pyenv virtualenv 3.8.5 ansible
pyenv local ansible

# If the virtualenv is correctly activated
python --version should return 3.8.5

pip install -r requirements.txt
