# 🌱 Sistema de Sensoriamento Agrícola  
Trabalho desenvolvido para a disciplina de **Banco de Dados** – FIAP

## 📌 Atividade 1: Entidades e Atributos

### 🧾 Entidades

#### 1. Cultura
- `id_cultura` (PK) – Identificador único da cultura  
- `nome` – Nome da cultura (ex: soja, café)

#### 2. Sensor
- `id_sensor` (PK) – Identificador único do sensor  
- `tipo` – Tipo do sensor (umidade, pH, NPK)

#### 3. LeituraSensor
- `id_leitura` (PK) – Identificador único da leitura  
- `id_sensor` (FK) – Sensor responsável pela leitura  
- `id_cultura` (FK) – Cultura relacionada à leitura  
- `data_hora` – Data e hora da leitura  
- `valor_medido` – Valor registrado pelo sensor

#### 4. AplicacaoProduto
- `id_aplicacao` (PK) – Identificador único da aplicação  
- `id_cultura` (FK) – Cultura que recebeu a aplicação  
- `data_hora` – Data e hora da aplicação  
- `tipo_produto` – Tipo de produto aplicado (água, fertilizante, etc.)  
- `quantidade` – Quantidade aplicada

---

## 🔗 Relacionamentos

- Uma **Cultura** pode ter várias **LeiturasSensor** (1:N)  
- Um **Sensor** pode gerar várias **LeiturasSensor** (1:N)  
- Uma **Cultura** pode receber várias **AplicacoesProduto** (1:N)

---

## 📊 Tipos de Dados Sugeridos

| Atributo                         | Tipo de Dado       |
|----------------------------------|--------------------|
| `id_*`                           | INTEGER            |
| `nome`, `tipo`, `tipo_produto`  | VARCHAR(100)       |
| `data_hora`                      | DATETIME           |
| `valor_medido`, `quantidade`     | DOUBLE             |

---

## ❗ Observações

Devido a limitações técnicas, **não foi possível utilizar o Oracle SQL Developer Data Modeler** para gerar o arquivo `.dmd`.  
A modelagem foi realizada manualmente com base nos requisitos do trabalho e nos conceitos abordados durante a disciplina.

---

## 📁 Estrutura do Projeto

- `README.md` – Documentação do projeto  
- `diagramas/` – (Opcional) Imagens dos diagramas MER e DER  
- `scripts_sql/` – (Futuramente) Scripts SQL de criação e manipulação das tabelas  
- `relatorios/` – (Opcional) Relatórios e arquivos auxiliares

---

## 💡 Objetivo do Sistema

O sistema tem como objetivo gerenciar informações de sensores aplicados em plantações, permitindo o acompanhamento de leituras ambientais (como umidade, pH e nutrientes) e o controle das aplicações de insumos (água, fertilizantes, entre outros) por cultura agrícola.



