# 🌾 **Modelagem de Banco de Dados para Sistema de Sensores Agrícolas**

## 📄 **Descrição**
Bem-vindo ao repositório de modelagem de banco de dados para um **sistema de sensores agrícolas**. Este sistema foi projetado para coletar e analisar dados de sensores que monitoram as condições de cultivo, como:

- **Umidade do solo** 🌧️
- **pH do solo** ⚖️
- **Nutrientes essenciais** (fósforo e potássio) 🌱

O objetivo principal é **otimizar o uso de água e nutrientes nas plantações**, garantindo uma gestão eficiente e sustentável dos recursos agrícolas.

## 🎯 **Objetivo do Projeto**
O objetivo deste projeto é desenvolver a **modelagem de um banco de dados** utilizando **MER** (Modelo Entidade-Relacionamento) e **DER** (Diagrama Entidade-Relacionamento), para armazenar e analisar dados de sensores agrícolas, com o foco de:

- Otimizar o uso de **água** 💧
- Controlar a **aplicação de nutrientes** 🌿
- Monitorar a **saúde do solo** 🌾

A modelagem segue os princípios de relacionamento de bancos de dados, incluindo os tipos de relacionamentos **1:N** (um para muitos) e **N:N** (muitos para muitos).

## 🛠️ **Tecnologias e Ferramentas Usadas**
- **SQL Developer Data Modeler**: Ferramenta utilizada para criar os diagramas MER e DER do banco de dados.
- **GitHub**: Repositório utilizado para versionamento, colaboração e armazenamento do projeto.
- **Markdown**: Utilizado para a documentação do repositório.
- **Python**: Linguagem de programação usada para a manipulação e análise de dados (se aplicável).
- **Pandas**: Biblioteca Python utilizada para manipulação de dados em tabelas.
- **Oracle**: Sistema de banco de dados utilizado para gerenciar a modelagem e dados de sensores.

## 🚀 **Como Rodar o Projeto**
Este repositório contém a modelagem de banco de dados para o sistema de sensores agrícolas. O foco principal está na criação e documentação da estrutura do banco de dados, incluindo os diagramas MER e DER.

No entanto, se você desejar interagir com o banco de dados ou executar consultas, será necessário importar o modelo de banco de dados (arquivo .dmd do SQL Developer Data Modeler) para uma ferramenta como o SQL Developer ou Oracle para poder criar o banco de dados fisicamente e executar as operações desejadas.

Baixe o arquivo de modelagem: Acesse o repositório para obter o arquivo de modelagem do banco de dados, com o diagrama MER e DER.

Ferramentas Necessárias:

SQL Developer: Para visualizar a modelagem ou gerar o script SQL.

Oracle (se aplicável) ou qualquer outro banco de dados compatível, para criar o banco de dados real.

Importação da Modelagem:

Importe o arquivo .dmd no SQL Developer ou outra ferramenta de modelagem compatível para visualizar e modificar o modelo.

Criação do Banco de Dados:

Caso você queira criar o banco de dados real, utilize o SQL gerado pelo SQL Developer ou Oracle para criar as tabelas no seu banco de dados.

Consultas e Testes:

Após a criação do banco, você pode rodar consultas SQL para testar o funcionamento e verificar a integridade dos dados.

## 📊 **Diagrama Entidade-Relacionamento (DER)**
O diagrama a seguir ilustra a modelagem do banco de dados para o sistema de sensores agrícolas, incluindo as entidades e seus relacionamentos.


**🔑 Entidades Principais:**
- Sensores (umidade, pH, nutrientes)
- Dados coletados
- Ajustes de irrigação e aplicação de nutrientes
- Culturas agrícolas

**🔗 Relacionamentos:**
- Sensores coletam dados para cada cultura.
- Ajustes de irrigação aplicam-se a cada sensor e cultura.

## 🤝 **Instruções de Contribuição**
Se você deseja contribuir para este projeto, siga os passos abaixo:
1. Faça um **fork** deste repositório.
2. Implemente as melhorias ou ajustes desejados.
3. Envie uma **pull request** para revisão.

Contribuições são bem-vindas, e agradecemos o seu interesse!

## 📜 **Licença**
Este projeto está licenciado sob a **Licença MIT**.

## 📚 **Referências**
- **SQL Developer Data Modeler**
- **Livros e materiais** sobre modelagem de banco de dados.



