# Dataset-FactPolCheckBr
Repositório contendo dataset respectivo a dados de fake news obtidas a partir de um conjunto de diferentes fontes.

# Dados
Os dados em formato CSV (sem texto da checagem e com texto da checagem) podem ser encontrados no diretório "dados". Cada entrada (linha de tabela) destes arquivos corresponde a uma instância de checagem.

Os dados sem texto da checagem estão separados eem 10 arquivos, por agência de checagem:

| Arquivo              | Tipo                     | n° entradas      |
|----------------------|--------------------------|-----------------:|
| AFP_Checamos.csv     | csv                      | 196              |
| Aos_Fatos.csv        | csv                      | 310              |
| Boatos.org.csv       | csv                      | 313              |
| CNJ.csv              | csv                      | 10               |
| E-farsas.csv         | csv                      | 50               |
| Fato_ou_Boato.csv    | csv                      | 184              |
| Fato_ou_Fake.csv     | csv                      | 171              |
| Lupa.csv             | csv                      | 245              |
| Projeto_Comprova.csv | csv                      | 175              |
| UOL_Confere.csv      | csv                      | 228              |

Cada arquivo possui uma tabela (csv) com as seguintes colunas:

| Coluna                                         | Definição                                                                                           | Tipo                         |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------|-----------------------------:|
| Título da checagem                             | Nome da checagem (atribuído pela agência)                                                           | string                       |
| Data da checagem                               | Data (mês/dia/ano) em que foi realizada a checagem                                                  | date                         |
| Natureza da notícia                            | Veracidade da notícia checada (Falsa, Verdadeira, Parcialmente verdadeira, etc.), segundo a agência | string                       |
| Candidato(s) favorecidos(s) pela notícia falsa | Nomes dos candidatos eleitorais favorecidos pela notícia (caso falsa)                               | string                       |
| Agência                                        | Nome da agência de checagem                                                                         | string                       |
| Link                                           | url da página específica à checagem no site da agência                                              | string                       |

---

Os dados que incluem os textos das checagens estão agregados no arquivo com_texto.csv. Este arquivo combina as entradas dos 10 arquivos anteriores e adiciona o texto de cada checagem:

| Arquivo              | Tipo                     | n° entradas      |
|----------------------|--------------------------|-----------------:|
| com_texto.csv        | csv                      | 1882             |

O arquivo possui uma tabela (csv) com as mesmas colunas presentes nos outros arquivos, com a adição e uma nova coluna, contendo o texto que contextualiza a checagem e a notícia checada pela agência, extraído do site da agência de checagem:

| Coluna                          | Definição                                                                  | Tipo                         |
|---------------------------------|----------------------------------------------------------------------------|-----------------------------:|
| ...                             | ...                                                                        | ...                          |
| texto                           | texto contextualizando checagem e notícia checada (publicado pela agência) | string                       |

# Visualização
Para simples visualização (dados sem texto da checagem), baixe o conteúdo do diretório "visualizacao" e abra o arquivo index.html (requer navegador).

# Licença
<p xmlns:cc="http://creativecommons.org/ns#" ><a rel="cc:attributionURL" href="https://github.com/Interfaces-UFSCAR/Dataset-FakeNews">This work</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="http:// dgp.cnpq.br/dgp/espelhogrupo/5226786888084066">Interfaces - Núcleo de Estudos Sociopolíticos dos Algoritmos e da Inteligência Artificial</a> is licensed under <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>
