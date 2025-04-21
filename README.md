# 🌾 FarmTech Solutions – Sensoriamento para Irrigação e Nutrientes 🌱

## 🧠 Sobre o Projeto
Este repositório contém a modelagem de banco de dados relacional desenvolvida para a disciplina de Banco de Dados da FIAP (Capítulos 10 ao 12), focada no uso de sensores em plantações para otimizar a irrigação e aplicação de nutrientes.

O sistema visa:
- 📡 Armazenar dados dos sensores de umidade, pH e nutrientes.
- 💧 Monitorar e ajustar automaticamente a irrigação e fertilização.
- 📊 Analisar variações ao longo do tempo para decisões mais inteligentes.

---

## 🔍 Objetivos
- Criar um modelo de banco de dados eficiente e relacional.
- Otimizar o uso de recursos hídricos e nutricionais.
- Permitir análises históricas das medições dos sensores.

---

## 📌 Requisitos do Sistema
O sistema precisa responder a perguntas como:
- 🗓️ **Qual foi a quantidade total de água aplicada em cada mês?**
  - Dados necessários: Data, Hora e Quantidade de Água Aplicada.
- 🌡️ **Como variou o pH do solo ao longo do ano?**
  - Dados necessários: Data, Hora e Valor do pH.
- 🧪 **Quais nutrientes foram aplicados e em que quantidade?**
  - Dados necessários: Data, Hora e Quantidade de NPK aplicada.

---

## 🧱 MER – Modelo Entidade Relacionamento

### 🎯 Entidades e Atributos

#### 🌽 Plantações
- `id_plantacao` (PK) - Inteiro
- `nome_cultura` - Texto
- `localizacao` - Texto

#### 📦 Sensores
- `id_sensor` (PK) - Inteiro
- `tipo_sensor` - Texto (`Umidade`, `pH`, `Nutrientes`)
- `descricao` - Texto

#### 📈 Leituras
- `id_leitura` (PK) - Inteiro
- `data_hora` - DateTime
- `valor` - Double
- `id_sensor` (FK) - Inteiro
- `id_plantacao` (FK) - Inteiro

#### 🚿 Aplicações de Água
- `id_aplicacao` (PK) - Inteiro
- `data_hora` - DateTime
- `quantidade_litros` - Double
- `id_plantacao` (FK) - Inteiro

#### 🧴 Aplicações de Nutrientes
- `id_nutriente` (PK) - Inteiro
- `data_hora` - DateTime
- `quantidade_nutriente` - Double
- `tipo_nutriente` - Texto (`Fósforo`, `Potássio`, etc.)
- `id_plantacao` (FK) - Inteiro

---

## 🔗 Relacionamentos

- Uma **Plantação** 🌽 pode ter muitos **Sensores** 📦 (1:N)
- Um **Sensor** 📦 pode gerar muitas **Leituras** 📈 (1:N)
- Uma **Plantação** 🌽 pode ter muitas **Aplicações de Água** 🚿 (1:N)
- Uma **Plantação** 🌽 pode ter muitas **Aplicações de Nutrientes** 🧴 (1:N)

---

## 🧠 Tipo dos Dados (Cap. 12)

| Atributo              | Tipo de Dado  |
|-----------------------|---------------|
| `id_plantacao`        | INT           |
| `nome_cultura`        | VARCHAR(100)  |
| `localizacao`         | VARCHAR(100)  |
| `id_sensor`           | INT           |
| `tipo_sensor`         | VARCHAR(50)   |
| `descricao`           | TEXT          |
| `id_leitura`          | INT           |
| `data_hora`           | DATETIME      |
| `valor`               | DOUBLE        |
| `quantidade_litros`   | DOUBLE        |
| `quantidade_nutriente`| DOUBLE        |
| `tipo_nutriente`      | VARCHAR(50)   |

---

## 📦 Entrega

📁 O repositório contém:
- ✅ Arquivo `.dmd` (modelo criado no SQL Developer Data Modeler)
- ✅ Imagem `.png` do DER
- ✅ Este arquivo `README.md` com a documentação completa do MER
