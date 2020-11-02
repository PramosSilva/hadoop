# Instalando Pyspark no Linux

Este tutorial pressupõe que esteja instalado o Anaconda.

## Instalar o JDK 1.8

No meu caso eu tive problema com o JDK pois existia uma outra versão instalada na máquina.  
Para corrigir este erro, primeiro liste as versões do java que estão instaladas e selecione a desejada.
```
sudo update-alternatives --config java
```

No meu caso eu instalei utilizando o comando apt e repeti o processo acima para selecionar a nova versão instalada.
```
sudo apt install openjdk-8-jdk
```

## Instalar Spark

O download pode ser feito no site [Apache Spark](https://spark.apache.org/downloads.html).  
Após baixar o arquivo, descompacte utilizando o código a seguir: 
```
tar -xvf spark-version
```
Lembrando que a *version* deve ser substituida pela versão do arquivo que foi baixada.  
Mova o arquivo descompactado para a pasta spark que será criada no diretório opt.
```
mv spark-version /opt/spark
```
Agora volte ao diretório **home** e edite o arquivo *.bashrc*.
```
gedit .bashrc
```
Vá até o final do arquivo e acrescente o seguinte código.
É preciso passar o caminho do JDK e do Spark que foi instalado na máquina. 
```
# JDK
export JDK_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre/bin
export PATH=$PATH:$JDK_HOME/bin

# Spark
export SPARK_HOME=/opt/spark
export PATH=$PATH:$SPARK_HOME/bin
export PYSPARK_PYTHON=python3
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS=notebook
```
Atualize o arquivo.

```
source .bashrc
```

Verificque se esta funcionando corretamente. Abra o terminal e execute o comando.

```
pyspark
```
Ele deverá abrir a tela do jupyter notebook. Digite em um célula o seguinte comanto.
```
sc
```
Deverá ser retornado a versão instalada.
```
SparkContext

Spark UI

Version
v3.0.1
Master
local[*]
AppName
PySparkShell
```
