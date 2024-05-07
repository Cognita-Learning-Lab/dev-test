## Teste de programação da Cognita:

### Apresentação

Site da empresa: https://cognita.com.br/

Ao ser escolhido para a vaga, irá trabalhar nessa aplicação: https://unicte.com/ 

O app Cognittron é uma plataforma de cursos diferenciada por seus mapas visuais e aprendizado prático, buscando diminuir a taxa de abandono das plataformas de cursos tradicionais. 


### As tarefas

Vamos primeiro criar alguns nós no nosso banco Neo4j, se não conhece Cypher (a linguagem do Neo4j), não se assuste, é simples na maioria dos casos. Abaixo estamos criando um nó para cada label, os labels são "Step" "Trail", "Theme" e "Academy", pode pensar nos Labels como classes em Javascript ou qualquer outra linguagem:

```cypher
CREATE (s:Step { 
	id: 'step-1', 
	title: 'O primeiro passo', 
	content: 'O conteúdo do primeiro passo' 
})
CREATE (t:Trail {
	id: 'trail-1',
	title: 'A primeira trilha'
})  
CREATE (tm:Theme {
	id: 'theme-1',
	title: 'O primeiro tema'
})
CREATE (a:Academy {
	id: 'academy-1',
	title: 'A primeira academia'
})
```

Vamos para a primeira tarefa, agora que temos nossos nós no banco, precisamos de criar as relações, e isso que diferencia dos objetos Javascript, no Neo4j temos relações entre os nós, que é bem simples de criar, mas é com você, crie as seguintes relações, pode criar elas no loader da rota junto com o código acima, mas lembre-se de não criar os nós e as relações se já existirem:

```
Uma trilha tem passos
Um tema tem trilhas
Uma academia tem temas
```

Após ter criados essas relações, estamos prontos para prosseguir e criar nossa rota "/explore/<trailId>" no Remix, usamos o Remix versão 2.

A segunda tarefa é buscar todos os passos da trilha, e mostrar na tela o título dos passos e o conteúdo, como também o título da trilha uma única vez em cima de todos os passos.

A terceira tarefa é implementar um botão para criar um novo passo. Podendo passar o id, o título e o conteúdo do passo. Ao clicar em criar, deve adicionar esse passo no banco. 

A parte visual das tarefas deve usar React / TailwindCSS e seguir o design do Figma (copie o projeto para sua conta do Figma e acione o modo dev do Figma para ver as propriedades CSS): https://www.figma.com/file/FDIkxUdJuq034npFEcurBi/Cognittron---Teste-Dev-01

### A entrega

Ao finalizar as tarefas, envie o link do repositório público Github para diogo@cognita.com.br com o assunto "Teste de programação Cognita - Seu Nome". O prazo é até dia 12/05/2024 às 22h, no horário de Brasília. Se quiser pode usar typescript ou não, como preferir, todo o código deve estar em inglês, e a rota deve estar funcionando, ou seja, quando dermos `npm run dev`, deve rodar o server, e a rota `http://localhost:3000/explore/trail-1` precisa estar funcionando sem erros e visualmente como no Figma.


### O pipeline React + Remix + Neo4j

Para aprender sobre React: https://react.dev/learn

Para começar com o Remix: https://remix.run/docs/en/main/start/quickstart

Aqui um arquivo simples de rota, com action e loader, que pode ser usado como base: https://remix.run/docs/en/main/route/action

Para instalar o Neo4j: https://neo4j.com/download/

Você pode retornar objetos Javascript caso não queira perder tempo instalando e entendendo como funciona a conexão com o Neo4j, mas deixe comentado como seriam as queries em Cypher em cada função que deveria interagir com o banco.


### Dúvidas?

Qualquer dúvida, pode me enviar uma mensagem no Linkedin: 

https://www.linkedin.com/in/diogohartuiqdebarba/



