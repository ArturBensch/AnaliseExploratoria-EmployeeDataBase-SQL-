# Análise Exploratória Employee DataBase (SQL)
Projeto desenvolvido para demonstrar as habilidades e técnicas com SQL

## Estudo da Base e o Modelo Relacional 

![image](https://github.com/user-attachments/assets/1fee0b48-6dc6-4807-a502-57dc96ae691d)

**Descrição das Tabelas:**

1)**Employees** – Contém dados dos funcionários, como ID (emp_no), nome, data de nascimento, gênero e data de contratação.

2)**Departments** – Lista os departamentos da empresa, identificados por um código (dept_no) e um nome (dept_name).

3)**Dept_emp** – Relaciona funcionários aos departamentos onde trabalharam ao longo do tempo.

4)**Dept_manager** – Armazena informações sobre os gerentes de cada departamento e o período em que exerceram essa função.

5)**Salaries** – Histórico de salários dos funcionários, indicando o valor (salary) e o período de validade.

6)**Titles** – Registra os cargos (title) que cada funcionário ocupou ao longo do tempo.

 Relacionamentos Importantes:
- A tabela employees se conecta com salaries, titles, dept_emp e dept_manager usando emp_no como chave primária.
- A tabela departments se relaciona com dept_emp e dept_manager através de dept_no.
- As tabelas salaries, titles, dept_emp e dept_manager possuem colunas de datas (from_date, to_date) para registrar mudanças ao longo do tempo.
