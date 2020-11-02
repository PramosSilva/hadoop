# Instalando Pyspark no Linux

## Instalar o JDK 1.8

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
```
# JDK

```
