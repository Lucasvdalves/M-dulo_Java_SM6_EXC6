# M-dulo_Java_SM6_EXC6

# Exercicio referente ao módulo de Java

1 --- Escreva um novo Servlet que receba como parâmetro em sua URL o nome de um determinado usuário e, em seguida, retorna uma mensagem de boas vindas para ele.
      O endereço final da requisição deve se parecer com este:
      http://localhost:8080/clamed/hello?name={nome do usuário}

2 -- Como ainda não entramos no mérito de banco de dados e aqui o foco são os Servlets, aqui você irá criar uma classe que representa uma tarefa.
      Os atributos devem ser:
     Identificador
     Descrição
     Status (pendente, em andamento ou concluída)
     Prioridade (baixa, média ou alta)
     Nome do responsável

3 --    Crie uma classe Java que represente um banco de dados fictício. Ela deve contemplar uma lista estática que conterá as tarefas cadastradas.
        Você deve criar os métodos para:
        Salvar uma tarefa na lista.
        Remover uma tarefa da lista com base no identificador.
        Listar as tarefas cadastradas.
        Listar as tarefas cadastradas com base no status fornecido.
        Listar as tarefas cadastradas com base na prioridade.
        Listar as tarefas cadastradas com base no responsável.

4 --    Por se tratar de uma API, você não precisará criar o formulário via JSP ou configurar rotas para exibir o formulário.
        A requisição de cadastro deve ser realizada por meio do Postman, enviando um objeto JSON em uma requisição POST
        O JSON deve conter todos os atributos que a entidade requisita, com exceção do identificador.
        O identificador deve ser gerado automaticamente de forma incremental em seu back-end, ou seja, você deve criar a lógica de negócios para que cada item tenha um identificador único e em ordem crescente.
        Seu Servlet deve conter um método POST que lida com a requisição.  

5 --    Os usuários irão consumir informações de sua API, então eles desejam listar via Postman as tarefas cadastradas, obtendo um retorno em formato JSON.
        Eles também desejam utilizar filtros para obter apenas as tarefas de determinado responsável, status ou prioridade. Caso nenhum filtro seja passado, deve ser retornada apenas a lista com todas as tarefas.      
        O Servlet deve conter um método que lide com requisições de tipo GET para essa operação.

        GET http://localhost:8080/clamed/task

        GET http://localhost:8080/clamed/task?status=PENDING

        GET http://localhost:8080/clamed/task?priority=HIGH

        GET http://localhost:8080/clamed/task?owner=Lucas  

6 --    Deve ser possível alterar uma determinada tarefa. Informações como descrição, nome do responsável, status e prioridade podem ser alterados.
        O Servlet deve ser de tipo PUT e deve receber o objeto a ser alterado em formato JSON, além de receber como parâmetro de URL qual o identificador da tarefa que será alterada.
        

7 -- Deve ser possível, com base em um identificador, remover uma tarefa. O identificador deve ser fornecido por meio da URL, sendo um parâmetro.
     A requisição deve ser de tipo DELETE, e o Servlet deve ter o método correto para o processamento dessa solicitação.
      
