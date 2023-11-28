# spring-boot-thymeleaf-exemplo
Exemplo de integração front-end usando Spring Boot e Thymeleaf

Classe ProdutoController

Esta é a classe do controlador que basicamente controla o fluxo dos dados. 
Ele controla o fluxo de dados no objeto do modelo e atualiza a visualização sempre que os dados são alterados. 
Então aqui estamos mapeando nossos dados de objeto com Thymeleaf.

Quando o usuário digita a URL localhost:8080/ no navegador a solicitação vai para o método viewHomePage() 
e neste método estamos buscando a lista de produtos e adicionando-a ao modal com chave, par de valores e retornando a página index.html. 

Na página index.html, a chave (allemplist) é identificada como um objeto java e o Thymeleaf itera sobre a lista e gera conteúdo dinâmico de acordo com o modelo fornecido pelo usuário.

/addNew – quando o usuário clica no botão Adicionar Produto, a solicitação vai para o método addNewProduto(). 
E neste método simplesmente criamos o objeto vazio do produto e o enviamos de volta para novoproduto.html para que o usuário possa preencher os dados neste objeto vazio e quando o usuário clica no botão salvar, 
o mapeamento /save é executado e obtém o objeto do produto e salve esse objeto no banco de dados.

/showFormForUpdate/{id} – Este mapeamento é para atualizar os dados existentes dos produtos.

/deleteProduto/{id} – Este mapeamento serve para excluir os dados existentes dos produtos.
