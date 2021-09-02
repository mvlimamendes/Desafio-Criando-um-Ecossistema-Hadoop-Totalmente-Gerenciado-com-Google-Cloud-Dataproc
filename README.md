# Desafio Criando um Ecossistema Hadoop Totalmente Gerenciado com Google Cloud Dataproc
<div align="justify">Neste desafio do bootcamp, o objetivo principal era conhecer a plataforma de computação em nuvem da Google. Para isso foi configurado um cluster Hadoop através do Google Cloud Dataproc.</div>

## Google Cloud Dataproc

<div align="justify">O Google Cloud Dataproc é um serviço totalmente gerenciado e altamente escalonável para executar o Apache Spark, o Apache Flink, o Presto e mais de 30 ferramentas e frameworks de código aberto. Use o Dataproc para modernização do data lake, ETL e ciência de dados segura, em escala global, totalmente integrada ao Google Cloud e com custos bem menores [1].</div> 

## Preparação de Ambiente

<div align="justify">Para a realização do desafio, foi necessário primeiramente configurar um bucket pelo Cloud Storage onde os arquivos foram armazenados. </div><br />

  
<div align="justify">Para a criação do cluster no Dataproc foi necessário previamente ativar a API do serviço para poder utilizá-lo. Após a ativação, o cluster foi configurado da seguinte forma: tipo de cluster, no caso o padrão (1 nó mestre, N workers) com 1 nó mestre e 3 nós workers, a imagem do sistema operacional utilizado, a versão do Hadoop e do Spark , CPU e memória alocada nos nós e no YARN,  configuração de rede, ativação de gateway de componente para as interfaces web do Spark, YARN, datanote e namenode. Alguns componentes adicionais podem ser adicionados de acordo com a necessidade do projeto. Por exemplo serviços como HBase, Anaconda, Druid, Flink e Presto podem ser configurados e instalados junto ao cluster o que dá muita flexibilidade na criação do cluster dependendo da necessidade.</div>

## Workload

<div align="justify">A tarefa era enviar um job PySpark para o cluster no qual executava um script em python que lia um arquivo .txt e retornava um arquivo .csv com as palavras mais comuns e a quantidade que as mesmas aparecem no arquivo. O arquivo part-00000 foi retornado para o bucket criado no inicio do projeto no Cloud Storage que pode ser baixado como .csv contendo a lista de todas as palavras e o número de vezes que aparece no arquivo livro.txt. Com o arquivo part-00000.csv em maõs, foi criado um arquivo resultado.txt foi criado contendo as 10 palavras mais do livro. Ambos os arquivos part-00000.csv e resultado.txt no repositório do projeto.</div>

### Links

[1] https://cloud.google.com/dataproc




