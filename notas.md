# Anotações
Estas são todas as minhas anotações feitas do curso Django Web Framework e Django Rest Framework na Udemy, feito por Luiz Otávio.
 
Obs: Essas anotações não foram feitas com intuito de ser úteis ou ensinar algo a alguém. Elas são feitas exclusivamente para mim e para o meu aprendizado.
 
É melhor que tudo esteja escrito em inglês, tando o código quanto as anotações. Como já comecei em português, tentarei manter as notas em português, mas todo o resto em inglês.


## Django
Existe um comando pelo qual você pode consultar todos os comandos do Django, e também entender como eles funcionam. Digite `django-admin --help`, e todos os comandos irão aparecer em sua tela.

#### Criando uma pasta para seu projeto
Para inicar o seu projeto, digitie o seguinte comando: `django-admin startproject projeto .`. A palavra "projeto" é o nome que você quer dar para o seu projeto. O ponto após ele indica que esta pasta será criada na pasta atual. Se você não colocar o ponto, o Django irá criar uma pasta chamada "projeto" com outra pasta dentro com o mesmo nome. Geralmente só usaremos esse comando para esta exata função, e não veremos mais ele. Usaremos o comando `manage.py` para todas as outras funções.
 

#### Iniciando um servidor
Para iniciar um servidor, basta digitar o comando `python manage.py runserver` no terminal. Este comando vai te dar um link pelo qual você pode acessar o seu site. Para desativar o servidor, basta ir no terminal e apertar ctrl + c. Essa servidor é só para desenvolvimento. Quando você for lançar seu site, você terá que usar outro servidor.
 

#### Aprendendo sobre `urls.py`
O `urls.py` é a porta de entrada da nossa aplicação. Precisamos de um endereço para acessar um site, e no nosso caso, temos um IP por padrão. No `urls.py` você pode configurar os endereços do seu site. Por padrão, esta é a poção de endereço que você tem disponívil no seu site:

```
urlpatterns = [
    path('admin/', admin.site.urls),
]
```

A função `path()` recebe uma rota e uma função. A rota é o nome que você deseja, e a função é o que te levará para a parte desejada do site. Essas funções ficam em um app, mas só veremos isso mais adiante, então a função será criada no próprio arquivo `urls.py` para fins de ensino. 

Lembrando que se você for escrever esse código, o seu servidor não pode estar rodando. Se ele estiver, assim que você salvar o arquivo você provavelmente terá um erro. 

Em resumo, a função que você deve criar recebe uma "request HTTP", e ela deve retornar uma "response HTTP". Veremos mais sobre isso no futuro. Para enviar uma resposta, utilizaremos o módulo HTTP do Django, e colocaremos uma string dentro.

Código de exemplo:

```
from django.http import HttpResponse


def my_view(request):
    return HttpResponse("STRING")


urlpatterns = [
    path('admin/', admin.site.urls),
    path('about/', my_view),
]
```

Com esse código escrito, quando você iniciar seu servidor e clicar no link do seu site, você poderá digitar "/about" e irá ver o que você digitou na função `my_view()`.
 

## Ambientes Virtuais
Ambientes virtuais são pastas que são utilizadas para guardar um projeto e suas dependências.

Utilizando um ambiente virtual, você não vai precisar instalar uma versão global de alguma dependência no seu computador. Por exemplo, se você estiver mexendo em um programa que utiliza uma versão muito antiga do Python, você não vai precisar instalar aquela versão no seu computador e correr o risco de quebrar todos os outros programas que já foram feitos com a versão mais nova. Você pode utilizar um ambiente virtual com a versão mais antiga somente para aquele projeto que você precisa.
 

#### Como criar um ambiente virtual no Windows
Entre na pasta na qual você deseja criar um ambiente virtual e abra o CMD naquela pasta. Depois disso, digite o seguinte código no CMD:

`python -m venv venv`

Este comando criará uma pasta com tudo o que você precisa pro ambiente virtual. O último "venv" é o nome da pasta do ambiente virtual. Em teoria você pode colocar o nome que você quiser, mas na prática, é melhor deixar como venv.
 

#### Como ativar e desativar o ambiente virtual no Windows
Para ativar ou desativar um ambiente virtual no Windows basta abrir o terminal na pasta onde se encontra a pasta do seu ambiente virtual e escrever o seguinte comando: `venv\Scripts\activate`. Para desativar, escreva `venv\Scripts\deactivate`. Se der algum erro, você precisará permitir o uso de ambientes virtuais. Para fazer isso, pesquise por "Como permitir ambientes virtuais no Windows através do PowerShell" e corrija o erro.
