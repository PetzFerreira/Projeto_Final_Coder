# Projeto de conclusão de curso - Pipeline de manipulação de dados

## Descrição

Utilizando objetos de dados de três diferentes datas da API Brasil(1.0.0), foi estruturada pipeline ETL (Extract Transform Load) em linguagem Python, utilizando Jupyter notebook, com o objetivo de transformar os dados extraídos e uní-los em apenas um dataframe. O intuito é produzir uma tabela que correlacione as informações pertinentes de cada data, integrando os dados de diferentes fontes ou origens, e posteriormente alimentar um banco de dados com essas informações consolidadas. 


## Recursos

Extração: Os dados são extraídos de três datas da BrasilAPI (/banks/v1, /feriados/v1/{ano}, /ddd/v1/{ddd}).
Transformação: Os dados são tratados individualmente para melhor controle e, em seguida, relacionados para formar um único dataframe.
Carga: Os dados transformados são carregados em um banco de dados SQLite.
Alertas: Um sistema de alerta notifica falhas no processo de extração utilizando a biblioteca plyer.

## Setup

*Para reproduzir o projeto, primeiramente clone o repositório.
    - O repositório pode ser clonado diretamente utilizando o GitHub Desktop; basta clicar na opção 'Open with GitHub Desktop', que surge após clicar no botão '< > Code'. 
    - Também pode ser clonado fazendo o download do arquivo ZIP e extraindo diretamente na pasta desejada, bem como pode-se clonar utilizando diretamente o link URL através do comando git clone (URL: https://github.com/PetzFerreira/projeto_final_etl_coderhouse.git)

* Após clonagem, realizar sequência de etapas de preparo:
   
   - Criação de ambiente virtual de desenvolvimento

   Windows

   ```sh
   python -m venv venv
   venv\Scripts\activate
   ```

   Linux, macOS

   ```sh
   python -m venv venv
   source venv/bin/activate
   ```
* No terminal, utilize o seguinte comando para instalar as bibliotecas instaladas no projeto original:

   ```sh
   pip install -r requirements.txt
   ```

## Execução

Abra o arquivo editor nomeado como `main_pipeline.ipynb` e execute as células para visualização dos execuções.
A estrutura das células está montada de forma linear, para que a execução célula a célula retorne todas as funcionalidades corretamente.

## Disposição da Pipeline

1. *Importação de bibliotecas*
2. *Criação de Funções Úteis*
3. *Extração e Manipulação -'Banks'*
4. *Extração e Manipulação 'ddd'*
5. *Extração e Manipulação 'Feriados* Nacionais'
6. *Criação de arquivos de extensão csv a partir de Dataframes*
7. *Alimentação de database com as tabelas criadas*
8. *Reconexão com database para confirmação de dados salvos*
