# Anotações
Estas são todas as minhas anotações feitas do curso Django Web Framework e Django Rest Framework na Udemy, feito por Luiz Otávio.

Obs: Essas anotações não foram feitas com intuito de ser úteis ou ensinar algo a alguém. Elas são feitas exclusivamente para mim e para o meu aprendizado.
 

## Ambientes Virtuais
Ambientes virtuais são pastas que são utilizadas para guardar um projeto e suas dependências.

Utilizando um ambiente virtual, você não vai precisar instalar uma versão global de alguma dependência no seu computador. Por exemplo, se você estiver mexendo em um programa que utiliza uma versão muito antiga do Python, você não vai precisar instalar aquela versão no seu computador e correr o risco de quebrar todos os outros programas que já foram feitos com a versão mais nova. Você pode utilizar um ambiente virtual com a versão mais antiga somente para aquele projeto que você precisa.
 

#### Como criar um ambiente virtual no Windows
Entre na pasta na qual você deseja criar um ambiente virtual e abra o CMD naquela pasta. Depois disso, digite o seguinte código no CMD:

`python -m venv venv`

Este comando criará uma pasta com tudo o que você precisa pro ambiente virtual. O último "venv" é o nome da pasta do ambiente virtual. Em teoria você pode colocar o nome que você quiser, mas na prática, é melhor deixar como venv.
 

#### Como ativar e desativar o ambiente virtual no Windows
Para ativar ou desativar um ambiente virtual no Windows basta abrir o terminal na pasta onde se encontra a pasta do seu ambiente virtual e escrever o seguinte comando: `venv\Scripts\activate`. Para desativar, escreva `venv\Scripts\deactivate`. Se der algum erro, você precisará permitir o uso de ambientes virtuais. Para fazer isso, pesquise por "Como permitir ambientes virtuais no Windows através do PowerShell" e corrija o erro.
