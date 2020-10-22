VIEW
====

- Cria uma nova tabela virtual. A ``VIEW`` possibilita extrair informações específicas de uma tabela existente. 

- Quando não se necessita de todas as informações de uma tabela, solicita apenas algumas colunas. 

.. code-block:: sql
  :linenos:

  CREATE VIEW ClientesIdade
  AS
  SELECT ClienteNome,DATEDIFF(YEAR,ClienteNascimento,GETDATE()) AS Idade	FROM dbo.Clientes;
