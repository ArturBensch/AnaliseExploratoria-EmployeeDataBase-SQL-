# Análise Exploratória Employee DataBase (SQL)
Projeto desenvolvido para demonstrar as habilidades e técnicas com SQL

## Estudo da Base e o Modelo Relacional - Parte 1

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

## Análises Iniciais - Parte 2
O estudo foi desenvolvido de modo gradual, ocorrendo primeiro análises mais simples e se aprofundando conforme o dúvidas surgiam. 

  ### Total de Funcionários Ativos
![image](https://github.com/user-attachments/assets/66ec2dd3-1304-4d86-b666-5a53abdef62c)

Por meio dessa query, ao utilizar a função DISTINCT no ID do funcionário e filtrar pela data máxima de contratação, é possível identificar que o número de funcionários ativos é próximo de 240 mil.

  ### Média de Idade 
  ![image](https://github.com/user-attachments/assets/81c246b3-ef8a-4c91-a5cd-1eba9fb1fffe)

Foi realizado um cálculo utilizando a função CURDATE(), que retorna a data atual, subtraindo-a da data de nascimento (birth_date). Em seguida, aplicamos a função AVG() para calcular a média de idade. Por fim, utilizamos ROUND() para arredondar o resultado com duas casas decimais.

  ### Distribuição de Funcionários por Gênero
 ![image](https://github.com/user-attachments/assets/e60a20d1-efb9-431e-9097-17737d3ffc53)

  ### Distribuição por Titulo
  ![image](https://github.com/user-attachments/assets/2c516c0f-7e09-4ba8-9922-e17c403c993c)


O inner join realizado para juntar a tabela *employee* com a *dept_emp*, assim trazendo informaçoes de ambas as tabelas, desde que tenham a mesma chave.  

 ### Número de funcionários por departamento
  ![image](https://github.com/user-attachments/assets/d8dd4895-75c1-4541-bf30-cbfea12d75b2)
  
Aqui visualizamos que o setor de desenvolvimento é onde há maior quantidade de funcionários. 

  ### Salário Médio por Cargo 
 ![image](https://github.com/user-attachments/assets/6c684911-4c7a-4842-9d09-962d0c10e85f)

Essa query nos tras algumas respostas e novas duvidas para analisar, visto que senior staff e staff sao os que possuem os maiores salários na empresa. Com isso trazendo algumas características da empresa. 

 
  ### Diferença entre Senior Staff e Manager
 xxxxxxxxxxxxxxxxxxxxx

  ### View Tempo de Contrato 
![image](https://github.com/user-attachments/assets/e1f4cea2-1151-4541-9044-f576f43e8674)

Para essa vw trazer a resposta desejada, foi necessário a utilizaçao de *case*, *TIMESTAMPDIFF* e funções como *coalsce*, *max*, *curdate*.   

### Resultado da vw : 
![image](https://github.com/user-attachments/assets/1c41a962-dd94-4d03-a170-63e4130436e1)


  

  
