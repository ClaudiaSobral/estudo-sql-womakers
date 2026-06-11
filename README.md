1. JOINS (Junções)
Fácil
Exercício 1: Escreva uma consulta que retorne o nome do cliente (clientes.nome) e o ID do pedido (pedidos.id) para todos os clientes que fizeram pedidos. Use um INNER JOIN.

Exercício 2: Liste todos os produtos (produtos.nome) e, se houver, o nome da categoria (categorias.nome) à qual pertencem. Garanta que produtos sem categoria também apareçam.

Exercício 3: Exiba o nome dos funcionários e o nome de seus respectivos departamentos. Se um departamento não tiver funcionários, ele ainda deve aparecer na lista.

Exercício 4: Retorne o ID do pedido e o nome do método de envio (envios.metodo). Se o pedido não foi enviado ainda (campo de envio nulo), o pedido deve ser listado da mesma forma.

Exercício 5: Escreva uma consulta para correlacionar uma tabela de autores com livros. Mostre apenas os autores que possuem livros cadastrados.

Médio
Exercício 6: Encontre todos os clientes que nunca fizeram um pedido. Utilize LEFT JOIN e um filtro WHERE.

Exercício 7: Faça um SELF JOIN na tabela funcionarios para listar o nome de cada funcionário e o nome do seu respectivo supervisor (dica: a tabela possui as colunas id e supervisor_id).

Exercício 8: Junte as tabelas alunos, matriculas e cursos para retornar o nome do aluno e o nome do curso em que ele está matriculado.

Exercício 9: Retorne o nome do produto, o preço unitário e a quantidade total vendida (da tabela itens_pedido). Agrupe por produto.

Exercício 10: Combine as tabelas fornecedores e produtos. Exiba o nome do fornecedor e a quantidade de produtos distintos que ele fornece, mas apenas para fornecedores com mais de 5 produtos.

Difícil
Exercício 11: Crie um relatório com o FULL OUTER JOIN entre as tabelas vendas_2024 e vendas_2025 baseado no produto_id. Exiba o ID do produto e calcule a diferença de receita entre os dois anos (trate valores nulos como zero).

Exercício 12: Realize um CROSS JOIN entre uma tabela de cores e uma de tamanhos. Filtre o resultado para excluir combinações onde a cor seja 'Verde' e o tamanho seja 'P'.

Exercício 13: Junte as tabelas usuarios, logins e compras. Retorne os usuários que fizeram login nos últimos 30 dias, mas que não realizaram nenhuma compra nesse período.

Exercício 14: Você tem as tabelas projetos, funcionarios e uma tabela intermediária alocacoes. Escreva uma consulta que mostre o nome do projeto e o custo total de salários da equipe alocada nele.

Exercício 15: Utilizando JOINS múltiplos, liste os clientes que compraram produtos de todas as categorias disponíveis no sistema.

2. Subconsultas (Subqueries)
Fácil
Exercício 16: Encontre o nome de todos os produtos cujo preço seja maior que a média de preço de todos os produtos da tabela.

Exercício 17: Liste os IDs dos clientes que fizeram pedidos no dia '2026-06-01' usando uma subconsulta no WHERE com o operador IN.

Exercício 18: Selecione o nome dos funcionários que trabalham no departamento de 'TI', buscando o departamento_id através de uma subconsulta.

Exercício 19: Retorne o título do livro mais caro da biblioteca utilizando uma subconsulta para encontrar o preço máximo.

Exercício 20: Escreva uma consulta que retorne os dados dos clientes cujo saldo em conta seja menor que o saldo do cliente com ID 42.

Médio
Exercício 21: Liste os produtos (nome e preço) que são mais caros que o produto mais caro da categoria 'Eletrônicos'.

Exercício 22: Use uma subconsulta correlacionada para listar os funcionários que ganham mais do que a média salarial do seu próprio departamento.

Exercício 23: Encontre os clientes que realizaram mais de 3 pedidos utilizando uma subconsulta na cláusula FROM (derivando uma tabela temporária de contagem).

Exercício 24: Exiba o nome do produto e, em uma coluna ao lado (usando subconsulta no SELECT), a quantidade total que já foi vendida desse produto específico.

Exercício 25: Selecione as categorias de produtos que possuem pelo menos um produto com estoque zerado, utilizando o operador EXISTS.

Difícil
Exercício 26: Encontre os clientes cujos pedidos individuais sempre superam o valor médio de qualquer pedido feito no site (use ALL).

Exercício 27: Identifique os funcionários que receberam um bônus maior que a média de bônus de sua respectiva filial, mas apenas se a filial tiver mais de 10 funcionários.

Exercício 28: Escreva uma consulta utilizando subconsultas correlacionadas aninhadas para encontrar o segundo produto mais vendido de cada categoria.

Exercício 29: Crie uma lista de clientes e retorne a data do último pedido de cada um. Se o cliente não tiver pedidos, exiba 'Sem pedidos' (trate tipos de dados se necessário).

Exercício 30: Selecione os departamentos onde o maior salário é menor do que a média salarial da empresa inteira.

3. CTEs (Common Table Expressions)
Fácil
Exercício 31: Crie uma CTE chamada PrecoMedio que calcule a média de preço dos produtos. Na consulta principal, selecione os produtos com preço acima dessa média.

Exercício 32: Defina uma CTE que liste os funcionários contratados no ano atual. No bloco principal, conte quantos funcionários foram listados.

Exercício 33: Escreva uma CTE que filtre apenas os clientes ativos. Use essa CTE para fazer um JOIN com a tabela de vendas.

Exercício 34: Use uma CTE para extrair o ano e o mês de uma tabela de vendas. Na consulta principal, agrupe e some o valor total por ano e mês.

Exercício 35: Crie uma CTE que selecione apenas os livros de um autor específico e, no comando principal, liste os títulos em ordem alfabética.

Médio
Exercício 36: Crie duas CTEs na mesma consulta: uma para calcular a receita total por cliente e outra para calcular o número de pedidos por cliente. Junte-as na consulta final.

Exercício 37: Escreva uma consulta usando CTE para identificar o funcionário que gerou a maior receita de vendas no mês passado.

Exercício 38: Crie uma CTE que calcule a média de avaliações de produtos. Use-a para listar os produtos que estão com avaliação abaixo da média da sua própria categoria.

Exercício 39: Crie uma lista com o top 5 clientes que mais gastaram utilizando uma CTE. Na consulta principal, classifique-os por relevância.

Exercício 40: Escreva uma CTE para limpar dados: selecione registros de logs removendo espaços extras de strings (TRIM) e convertendo textos para minúsculo. Use o resultado no bloco principal.

Difícil
Exercício 41 (Recursiva): Escreva uma CTE Recursiva para gerar uma sequência de números de 1 a 100.

Exercício 42 (Recursiva): Dada uma tabela de funcionarios com hierarquia (id e gerente_id), use uma CTE recursiva para mapear a árvore organizacional e exibir o nível hierárquico (Nível 1, Nível 2, etc.) de cada um.

Exercício 43: Utilize uma CTE para calcular o faturamento acumulado diário de uma loja e use a consulta principal para calcular a variação percentual dia após dia.

Exercício 44 (Recursiva): Escreva uma CTE recursiva que encontre todos os destinos possíveis de voos partindo de uma cidade 'A', considerando conexões na tabela voos(origem, destino).

Exercício 45: Crie um pipeline de dados usando 3 CTEs encadeadas para: (1) Filtrar outliers de vendas, (2) Calcular médias móveis de 3 dias, e (3) Retornar apenas os dias onde a venda real superou a média móvel.

4. Tabelas Temporárias
Fácil
Exercício 46: Crie uma tabela temporária (ex: #ClientesAtivos ou TEMP TABLE) e insira nela os IDs e nomes dos clientes que fizeram compras nos últimos 90 dias.

Exercício 47: Remova a tabela temporária criada no exercício anterior de forma segura (usando DROP TABLE IF EXISTS).

Exercício 48: Crie uma tabela temporária populada com os dados de categorias de produtos e adicione uma nova linha manualmente usando INSERT INTO.

Exercício 49: Crie uma tabela temporária vazia especificando as colunas id INT e data_criacao DATE. Insira a data atual nela.

Exercício 50: Selecione todos os dados de uma tabela temporária de produtos em promoção ordenando pelo maior desconto.

Médio
Exercício 51: Crie uma tabela temporária com o total gasto por cada cliente. Em seguida, atualize (UPDATE) uma coluna de status nessa tabela temporária para 'VIP' para clientes que gastaram mais de R$ 5.000.

Exercício 52: Escreva um script que use uma tabela temporária para armazenar dados parciais de um relatório de estoque e depois faça um JOIN dessa tabela temporária com uma tabela física do banco de dados.

Exercício 53: Crie uma tabela temporária que contenha a contagem de acessos diários por página de um site. Filtre a tabela para manter apenas os dias de semana (segunda a sexta).

Exercício 54: Popule uma tabela temporária com a lista de e-mails duplicados encontrados na tabela de usuários para posterior auditoria.

Exercício 55: Crie uma tabela temporária para armazenar dados de vendas mensais de 2025 e adicione uma restrição (índice ou chave primária) na coluna de ID para otimizar buscas.

Difícil
Exercício 56: Escreva um script complexo onde você armazena o resultado de uma consulta demorada em uma tabela temporária e depois realiza três consultas analíticas diferentes baseadas exclusivamente nessa tabela temporária para economizar processamento.

Exercício 57: Crie uma tabela temporária para simular o fechamento de caixa de uma loja: insira dados de vendas, deduza taxas de cartão de crédito calculadas dinamicamente e exiba o saldo líquido final.

Exercício 58: Crie duas tabelas temporárias distintas (uma para créditos e outra para débitos de usuários). Escreva uma consulta final que junte ambas para extrair o balanço final por usuário, lidando com usuários que podem estar presentes em apenas uma das tabelas.

Exercício 59: Use uma tabela temporária dentro de um bloco de script para armazenar dados de logs antigos, delete os registros originais da tabela física baseando-se nos IDs da tabela temporária (operação de expurgo) e faça o backup dos dados deletados.

Exercício 60: Crie uma tabela temporária para calcular a comissão de vendedores de forma escalonada: se vendeu até 10k ganha 5%, se vendeu mais ganha 10%. Use múltiplos UPDATEs ou estruturas condicionais para calcular o valor final da comissão na tabela.

5. Window Functions (Funções de Janela)
Fácil
Exercício 61: Use ROW_NUMBER() para numerar todas as linhas da tabela de funcionários ordenando pelo salário de forma decrescente.

Exercício 62: Calcule o total acumulado (SUM() OVER) das vendas ao longo do tempo (ordenado pela data da venda).

Exercício 63: Retorne o valor médio de vendas por categoria de produto ao lado de cada registro individual usando AVG() OVER (PARTITION BY...).

Exercício 64: Liste os produtos e utilize RANK() para criar um ranking dos produtos mais caros dentro de cada categoria.

Exercício 65: Use MIN() e MAX() como funções de janela para mostrar o menor e o maior salário do departamento na mesma linha de cada funcionário.

Médio
Exercício 66: Qual a diferença entre RANK() e DENSE_RANK()? Escreva uma consulta que aplique ambas na coluna de pontuação de alunos para demonstrar a diferença prática.

Exercício 67: Use a função LAG() para exibir o valor da venda do dia anterior na linha da venda do dia atual (para o mesmo cliente).

Exercício 68: Use a função LEAD() para projetar o próximo salário de um funcionário caso ele receba uma promoção na sequência cronológica de aumentos.

Exercício 69: Calcule a média móvel das vendas dos últimos 3 dias (incluindo o dia atual) utilizando a cláusula ROWS BETWEEN 2 PRECEDING AND CURRENT ROW.

Exercício 70: Utilize NTILE(4) para dividir os produtos do estoque em 4 quartetos baseando-se na quantidade disponível (criando grupos de prioridade de reposição).

Difícil
Exercício 71: Encontre apenas os funcionários que possuem o segundo maior salário de seu departamento, utilizando uma Window Function dentro de uma subconsulta ou CTE para filtrar.

Exercício 72: Calcule a diferença percentual entre o valor da venda atual e a média das 5 vendas anteriores do mesmo produto.

Exercício 73: Encontre a maior sequência de dias consecutivos em que um usuário fez login, utilizando técnicas de diferenciação de ROW_NUMBER() com datas (gaps and islands).

Exercício 74: Use FIRST_VALUE() e LAST_VALUE() (com a especificação correta de janela/WINDOW FRAME) para identificar o primeiro e o último produto comprado por cada usuário em seu histórico.

Exercício 75: Crie um relatório de vendas onde você exibe o valor da venda, o total acumulado do mês corrente e o percentual que aquela venda representa em relação ao total acumulado até aquele momento do mês.

Se precisar da resolução/gabarito comentada de algum exercício específico ou de uma variação para um banco de dados específico (como PostgreSQL, MySQL ou SQL Server), é só pedir!