# 🐘 Projeto de Integração com Banco de Dados PostgreSQL

Este projeto conecta dois bancos de dados PostgreSQL, realiza operações de consulta e manipulação de dados, gerenciando informações de tabelas como Cooperativa, Leilao, Produto e Endereco. Utiliza as bibliotecas `psycopg2` e `pandas` para trabalhar com dados e operações em bancos de dados de maneira eficiente e dinâmica. 🚀

## ✨ Funcionalidades

- 🔗 Conexão com múltiplos bancos de dados PostgreSQL.
- 📝 Extração de dados de tabelas e armazenamento em DataFrames usando pandas.
- ➕ Inserção de novos registros nas tabelas a partir dos dados obtidos.
- ♻️ Atualização automática dos registros caso a inserção falhe.
- ✅ Gerenciamento de status de dados para controle de processamento.

## 🛠️ Tecnologias Utilizadas

- `psycopg2`: Conexão e manipulação de dados no PostgreSQL com SQL.
- `pandas`: Manipulação avançada de dados em tabelas.
- `dotenv`: Carregamento seguro de variáveis de ambiente a partir de arquivos `.env`.

## 🏗️ Estrutura do Código

- 🔐 **Carregamento das Variáveis de Ambiente**: Informações sensíveis como host, usuário e senha dos bancos de dados são carregadas de um arquivo `.env`.

- 🔗 **Conexão com os Bancos de Dados**: Usando as variáveis de ambiente, o código estabelece conexões com os dois bancos PostgreSQL.

- ⚙️ **Operações com Dados**:
  - Extração de dados das tabelas Cooperativa, Endereco, Leilao, Produto e Imagens.
  - Os dados são carregados em DataFrames para processamento e manipulação.
  - Inserção de dados extraídos em um segundo banco de dados.
  - Se a inserção falhar, é realizada uma atualização (UPDATE) dos registros existentes.

- 📊 **Atualização de Status**: Após a inserção ou atualização, o campo `dados_status` é ajustado para `False`, indicando que o dado foi processado.

## 📋 Pré-requisitos

- Python 3.x instalado 🐍
- PostgreSQL configurado e rodando 🐘
- Instale as dependências do Python usando o arquivo `requirements.txt`.

## 🚀 Instalação

1. Clone o repositório:

   ```bash
   git clone https://github.com/Recoope/RPA_BANCO
   ```

2. Crie e ative um ambiente virtual:

   ```bash
   python -m venv venv
   source venv/bin/activate  # No Windows: venv\Scripts\activate
   ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

4. Crie um arquivo `.env` com as configurações de conexão:

   ```bash
   DB_HOST1=seu_host
   DB_DATABASE1=seu_banco1
   DB_USER1=seu_usuario1
   DB_PASSWORD1=sua_senha1
   DB_PORT1=5432
   DB_HOST2=seu_host2
   DB_DATABASE2=seu_banco2
   DB_USER2=seu_usuario2
   DB_PASSWORD2=sua_senha2
   ```

## 🎯 Como Executar

Após a instalação e configuração, basta rodar o script principal:

```bash
python teste_transformador.py
```

Isso iniciará a conexão com os dois bancos de dados e o processamento de inserção/atualização dos registros.

## 👨‍💻 Autor

Desenvolvido por Henrique Lucareli. Se você tiver dúvidas ou sugestões, fique à vontade para entrar em contato! 😊