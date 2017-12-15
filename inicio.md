# Sistema de Informação Sobre a Mortalidade - SIM

Nesta etapa será dado início ao processo de estruturação do banco de dados do SIM para o período de 1979 a 2015. Os procedimentos adotados para a aquisição dos arquivos, identificação de estruturas e organização da base de dados será descrita passo a passo, com ênfase nos _scripts_ desenvolvidos no R e no PostgreSQl.

###Primeiro Passo: Obtenção de arquivos para identificação de estruturas

A falta de documentação que descreva as mudanças ocorridas no SIM ao longo dos anos de maneira completa faz necessário que, inicialmente, obtenhamos alguns arquivos do SIM com o intuito único de identificar as variáveis disponíveis em cada ano. Esta identificação será complementada pelos arquivos disponibilizados pelo DataSUS com a estrutura do SIM em anos específicos.

Para tornar o processo mais rápido vamos adquirir os arquivos do Acre, que são menores. Realizaremos o download dos arquivos direto do "ftp" do datasus e vamos suar a library "RCurl"

```{r}
library(RCurl)
url <- "ftp://ftp.datasus.gov.br/dissemin/publicos/SIM/CID9/DORES/"
lista <- strsplit(getURL(url),'\n') #identifica o conteúdo do url em uma lista de arquivos
ac <- grep('AC', lista[[1]], value=T)
ac <- gsub('.*(AC[1-2



temp <- tempdir () # seleciona um diretório temporário temp
lista <- grep(
arq <- paste
```
