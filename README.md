# Delivery Much Tech Challenge - PHP

Bem vindo(a)! Esse é o Delivery Much Tech Challenge.

Aqui você terá todas as informações para realizar o seu desafio.

O tempo sugerido para conclusão do desafio é de cinco dias, mas não é uma regra. Estamos mais interessados em observar a qualidade da solução do que o tempo.

Quando sua solução estiver pronta, envie um e-mail para `tech.challenge@deliverymuch.com.br` com o link do seu repositório no Github. Seu código será analisado pelo nosso time de engenheiros. Após a análise, enviaremos o feedback e as instruções dos próximos passos!

Bom desafio!

## O Desafio - Backend

Você deve construir uma API que recebe ingredientes como parâmetro de entrada em uma chamada GET e retorna uma lista de receitas.
Utilize as APIs públicas da RecipePuppy (http://www.recipepuppy.com/about/api/) e da Giphy (https://developers.giphy.com/docs/) para obter os dados necessários.

A API deve receber como parâmetro um conjunto de ingredientes (máximo 3) e deve retornar os itens utilizados para realizar a busca; e uma lista de receitas.

Cada item lista de receitas deve possuir 4 atributos:
- Título da receita;
- Lista de ingredientes;
- Link para acessar a receita;
- Link de um gif para a receita.


#### A Estrutura

A API possui apenas um endpoint, que deve respeitar a seguinte chamada:

`http://{HOST}/recipes/?i={ingredient_1},{ingredient_2}`

Exemplo:

`http://127.0.0.1/recipes/?i=onion,tomato`


A resposta dessa requisição deve seguir a seguinte estrutura:

```json
{
	"keywords": ["onion", "tomato"],
	"recipes": [{
		"title": "Greek Omelet with Feta",
		"ingredients": ["eggs", "feta cheese", "garlic", "red onions", "spinach", "tomato", "water"],
		"link": "http://www.kraftfoods.com/kf/recipes/greek-omelet-feta-104508.aspx",
		"gif": "https://media.giphy.com/media/xBRhcST67lI2c/giphy.gif"
	   },{
		"title": "Guacamole Dip Recipe",
		"ingredients": ["avocado", "onions", "tomato"],
		"link":"http://cookeatshare.com/recipes/guacamole-dip-2783",
		"gif":"https://media.giphy.com/media/I3eVhMpz8hns4/giphy.gif"
	   }
	]
}
```
## O Desafio - Frontend

Você deve construir uma tela em que seja possível digitar de 1 a 3 ingredientes e buscar receitas para esses ingredientes digitados. A tela deve mostrar a lista de receitas, como as informações das receitas serão apresentadas fica por sua conta!

## Requisitos

- Utilizar PHP+Laravel para criar a aplicação;
- Toda configuração e chaves de acesso (se necessário) devem ser acessadas em um arquivo de ambiente. Sua configuração deve estar documentada no README;
- Para obter o gif no Giphy, utilize o título da receita recebido pelo RecipePuppy;
- Os ingredientes recebidos pelo RecipePuppy são recebidos em String. Organize os ingredientes em um array e ordene esse array por ordem alfabética;
- Se algum dos serviços externos estiver indisponível o projeto deverá informar o usuário dessa indisponibilidade;
- Utilizar Docker para executar o projeto;
- Tela funcional com as informações recebidas da API;


# Critérios de Avaliação

### Entrega
- O projeto está completo para ser executado?
- O projeto atende ao que se propõe fazer?
- Todos requisitos foram atendidos?

### Boas Práticas
- O código está bem estruturado?
- O código está fluente na linguagem?
- O código faz o uso correto de Design Patterns?

### Documentação
- O código foi entregue com um arquivo de README claro de como se guiar?
- A documentação foi suficiente para executar o projeto?
- Os commits são pequenos e consistentes?
- As mensagens de commit são claras?

### Código Limpo
- O código possibilita expansão para novas funcionalidades?
- O código é Don't Repeat Yourself?
- O código é fácil de compreender?

### Controle de Qualidade
- O código possui configuração de lint?
- Bônus: O código possui testes unitários?

### UX
- Layout agradável
- Leiturabilidade
- Usabilidade