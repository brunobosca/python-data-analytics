# python-data-analytics


# Desafio de Projeto - Processando e Transformando Dados com PBI
### Query usada para junção dos colaboradores e respectivos nomes dos gerentes: 

SELECT e.Ssn AS employee_id,
       CONCAT(e.Fname, " ", e.Minit, " ", e.Lname) AS employee_full_name,
       e.Super_ssn AS manager_id,
       CONCAT(m.Fname, " ", m.Minit, " ", m.Lname) AS manager_full_name
FROM employee e
LEFT JOIN employee m ON e.Super_ssn = m.Ssn;

### Resposta item 14 - Instruções:

Temos que usar a mescla de consultas ao invés da adição porquê se adicionarmos a consulta de dept_locations dentro departament os dados serão empilhados e teremos muitos valores nulos, pois o número de colunas das tabelas é diferente. Nesse caso, como dito acima, temos que usar a mescla pois a mesma encontra um "match" entre as colunas que queremos e traz os dados correspondentes. Nessa mescla fiz o "match" pelo número do departamento.
