# 🌾 Sistema de Monitoramento Inteligente de Plantação - FarmTech Solutions

## 📘 Descrição

Este projeto foi desenvolvido como parte da disciplina de Banco de Dados da FIAP (Capítulos 10 a 12). Ele simula um sistema de sensores aplicados em plantações para monitoramento e aplicação inteligente de água e nutrientes, com foco em aumentar a produtividade agrícola e reduzir desperdícios.

---

## 🎯 Objetivo

Criar um modelo de banco de dados relacional utilizando o **SQL Developer Data Modeler**, seguindo as regras de relacionamento **1:N** e **N:N**, que permita armazenar e analisar dados coletados por sensores de:

- Umidade
- pH
- Níveis de nutrientes (NPK)

---

## 📦 Entidades e Atributos (MER)

### 🔹 Sensor
- `id_sensor` (PK, INT)
- `tipo_sensor` (VARCHAR)
- `localizacao` (VARCHAR)
- `data_instalacao` (DATE)

### 🔹 Leitura
- `id_leitura` (PK, INT)
- `data_hora` (DATETIME)
- `valor` (DOUBLE)
- `id_sensor` (FK)

### 🔹 Aplicacao
- `id_aplicacao` (PK, INT)
- `data_hora` (DATETIME)
- `tipo_produto` (VARCHAR)
- `quantidade` (DOUBLE)
- `id_sensor` (FK)

### 🔹 Cultura
- `id_cultura` (PK, INT)
- `nome_cultura` (VARCHAR)
- `tipo` (VARCHAR)
- `area_total` (DOUBLE)

### 🔹 Cultura_Sensor (entidade intermediária N:N)
- `id_cultura_sensor` (PK, INT)
- `id_cultura` (FK)
- `id_sensor` (FK)

---

## 🔗 Relacionamentos

- Um **sensor** pode gerar várias **leituras** (1:N)
- Um **sensor** pode estar associado a várias **culturas**, e uma cultura a vários sensores (N:N)
- Uma **aplicação** está relacionada a um sensor (1:N)

---

## 🛠️ Tecnologias e Ferramentas

- Oracle SQL Developer Data Modeler
- Oracle Database
- SQL
- Git & GitHub

---

## 🖼️ Modelo Relacional (DER)

> Veja o DER exportado do SQL Developer: `docs/DER_agro.png`

---

## 🧪 Scripts

Os scripts SQL estão localizados na pasta `src/` e incluem:
- Criação das tabelas (`criacao_tabelas.sql`)
- Inserção de dados simulados (`insercao_dados.sql`)

---


## 📎 Entrega

Este repositório faz parte da atividade avaliativa da FIAP. Nenhuma modificação será feita após a data de entrega conforme as diretrizes da disciplina.

