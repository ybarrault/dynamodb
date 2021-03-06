
# How to install python boto3 SDK for AWS
## What is boto?
Boto is the Amazon Web Services (AWS) SDK for Python. It enables Python developers to create, configure, and manage AWS services, such as EC2 and S3. Boto provides an easy to use, object-oriented API, as well as low-level access to AWS services. The latest version of boto is boto3 and in this series, we will cover boto3.

## Python Boto3 Installation on Linux

### Step 1: Install Python and PIP if not already installed.
```
## Check if Python is already installed.
python --version

## Install Python
## On Debian derivatives such as Ubuntu, use apt.
sudo apt-get install python

## On Red Hat and derivatives, use yum.
sudo yum install python

## On SUSE and derivatives, use zypper.
sudo zypper install python

## Install PIP
## On all linux OS flavours
curl -O https://bootstrap.pypa.io/get-pip.py
python get-pip.py --user

## Check PIP version
pip --version
```

### Step 2: Install Python Boto3.
```
## Install Python Boto3 using PIP
pip install boto3 --user
```
## Python Boto3 Installation on Mac OS

### Step 1: Install Python and PIP if not already installed.

```
## Install python and PIP using homebrew
xcode-select --install
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install python #also installs PIP

## Check python and pip versions
python --version
pip --version
```
### Step 2: Install Python Boto3.
```
## Install Python Boto3 using PIP
pip install boto3
```

## Python Boto3 Installation on Windows

### Step 1: Open PowerShell using admin and install Chocolatey.
```
## Install chocolatey
## open PowerShell using admin privilege and execute below command to install chocolatey
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
exit
```
### Step 2: Install Python Boto3.
```
## Open command prompt using admin privilege
## Check if the installation was successful
choco --version

## Install python using choco
choco install python

## Refresh the environment and check if python and pip installed successfully.
refreshenv
python --version
pip --version

## Install boto3
pip install boto3
```

To get more details on Python Boto3, please refer below AWS documentation

https://boto3.amazonaws.com/v1/documentation/api/latest/index.html

6.    Importez la bibliothèque Boto 3, puis vérifiez que tout fonctionne correctement. Cette étape nécessite que vous disposiez des stratégies d'autorisation configurées à l'étape 1. L'exemple de sortie suivant répertorie tous les compartiments Amazon Simple Storage Service (Amazon S3) du compte.

```
>>> import boto3           # no error
>>> s3 = boto3.resource('s3')
>>> for bucket in s3.buckets.all():
print(bucket.name)
>>> exit()
```

7.    Utilisez la commande deactivate pour quitter l'environnement virtuel.

```
(env) $ deactivate

$
```
## Test

Importez la bibliothèque Boto 3, puis vérifiez que tout fonctionne correctement. Cette étape nécessite que vous disposiez des stratégies d'autorisation avec votre compte AWS IAM. L'exemple de sortie suivant répertorie tous les compartiments Amazon Simple Storage Service (Amazon S3) du compte.

```
$ python
Python 2.7.18 (default, Aug  4 2020, 11:16:42) 
[GCC 9.3.0] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> import boto3           # no error
>>> s3 = boto3.resource('s3')
>>> for bucket in s3.buckets.all():
print(bucket.name)
>>> exit()
```

## Documentation

[Boto3 documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
