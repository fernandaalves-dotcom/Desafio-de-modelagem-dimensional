<img src="Star schema.png" width="800">
📊 Modelagem Dimensional – Análise de Professores

## 🎯 Objetivo

Este projeto tem como objetivo a construção de um modelo dimensional no formato **Star Schema**, com foco na análise dos dados relacionados aos professores, conforme proposto no desafio.

---

## 🧩 Estrutura do Modelo

O modelo foi estruturado com uma tabela fato central e tabelas dimensão ao seu redor, permitindo análises eficientes e organizadas.

### 🔹 Tabela Fato

**Fato_Oferta_Disciplina**

Representa os eventos de oferta de disciplinas ministradas por professores.

**Granularidade:**
Cada registro corresponde a uma disciplina ministrada por um professor em determinado curso e período.

**Principais medidas:**

* `qtd_oferta` → quantidade de ofertas (valor padrão = 1)
* `carga_horaria_disciplina` → carga horária da disciplina

---

### 🔹 Tabelas Dimensão

**Professor**

* Contém informações cadastrais e profissionais dos docentes
* Relaciona-se com o departamento ao qual pertence

**Disciplina**

* Armazena os dados das disciplinas ofertadas

**Curso**

* Representa os cursos nos quais as disciplinas são ministradas

**Departamento**

* Define a estrutura organizacional vinculada ao professor

**Tempo**

* Permite análises temporais (dia, mês, semestre, ano)
* Criada para suprir a ausência de dados temporais no modelo relacional original

---

## 🔗 Relacionamentos

* A tabela fato se relaciona com todas as dimensões principais:

  * Professor
  * Disciplina
  * Curso
  * Tempo

* O relacionamento com **Departamento** é realizado por meio da tabela **Professor**, evitando redundância e garantindo consistência dos dados.

---

## 🧠 Decisões de Modelagem

* O modelo foi desenvolvido seguindo o padrão **Star Schema**, com foco em simplicidade e desempenho analítico.
* A granularidade foi definida para permitir análises detalhadas por professor, disciplina e período.
* A dimensão tempo foi criada manualmente para possibilitar análises históricas.
* O departamento foi vinculado ao professor, evitando duplicidade de informação na tabela fato.

---

## 📈 Possíveis Análises

Com esse modelo, é possível realizar análises como:

* Quantidade de disciplinas ministradas por professor
* Carga horária total por docente
* Distribuição de disciplinas por curso
* Análise por período (mês, semestre, ano)
* Comparação entre departamentos

---

## ✅ Conclusão

O modelo desenvolvido atende aos requisitos do desafio, permitindo uma visão analítica clara e consistente dos dados relacionados aos professores, com estrutura adequada para suporte à tomada de decisão.

---

