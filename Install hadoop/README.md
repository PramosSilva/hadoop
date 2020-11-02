## Configurando Hadoop no Linux

Execute os códigos a seguir para atualizar e instalar alguns pacotes.
```
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install build-essential ssh lzop git rsync curl
sudo apt-get install python-dev python-setuptools
sudo apt-get install libcurl4-openssl-dev
sudo easy_install pip
sudo pip install virtualenv virtualenvwrapper python-dateutil

```

## Criando usuário para o Hadoop

Para garantir a segurança é recomendado criar um usuário sem acesso como administrador.

```
sudo addgroup hadoop
sudo adduser --ingroup hadoop hadoop

```
