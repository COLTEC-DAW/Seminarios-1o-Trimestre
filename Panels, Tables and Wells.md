
#Trabalho Bootstrap        


###Tables, Panels and Wells  

######Aluno: Ícaro Emídio Adão
___

##Tables

###Introdução

No bootstrap as tabelas podem ser ativadas através da classe `.table` em qualquer     
`<table>`. Esse componente é composto básicamente do header e do body, que por sua 
vez são estruturados dentro da tag `<table>` como `<header>` e `<body>`, respectivamente. 
O escopo das tabelas podem ser definidas como colunas ou lacunas, o que muda a 
orientação da leitura dos dados. As tabelas estão dispostas à diversos tipos de 
alterações,os exemplos e suas classes responsáveis vem a seguir.


####Especifícação de Cores
        
A classe `.table-dark` inverte as cores da tabela padrão para fundo preto e cores brancas.
Sua declaração vem logo após a tag `<table>`.

Exemplo: 

```html            
<table class="table table-dark">
```

A alteração também pode ser aplicada no header da tabela, com a classe `.thead-dark` e
`.thead-light`.
        
Exemplo:

```html  
<table class="table">
        <thead class="thead-dark">
        </thead>
</table>
```
[Table Default](https://jsfiddle.net/IcaroColtec/3tL50stk/)        
[Table Dark](https://jsfiddle.net/IcaroColtec/4n3fn0vt/)

####Lacunas com estilos e cores diferentes

Essa alteração pode ser feita através da classe `.table-striped`. A declaração da classe
vem logo após a declaração da `<table>`. Ela aceita também a classe `.table-dark`.

Exemplo:

```html  
<table class="table table-striped">
  <thead>
    <tr>
      <th scope="col">Nome/th>
      <th scope="col">N° da matrícula</th>
      <th scope="col">Ano de Ingressão</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Ícaro</th>
      <td>16000000</td>
      <td >2016</th>
    </tr>
    <tr>
      <th scope="row">Fulano</th>
      <td>16111111</td>
      <td >2013</th>
    </tr>
  </tbody>
</table>
```
[Stripped Colums](https://jsfiddle.net/IcaroColtec/6kjqwthv/)

####Inserção de Bordas ou tabelas sem divisão de lacunas

A classe `.table-bordered` é a responsável por essa 
alteração, novamente também aceita a versão `.table-dark`.

Exemplo:

```html
<table class="table table-bordered">
  <thead>...</thead>
  <tbody>...</tbody>
</table>
```
[Bordered Table](https://jsfiddle.net/IcaroColtec/94f8064k/)

####Inserção de hover nas lacunas

Feita através da classe `.table-hover`, afeta todas as 
lacunas exceto o header da tabela. 

Exemplo:

```html
<table class="table table-hover">
  <thead>...</thead>
  <tbody>...</tbody>
</table>
```
[Table Hover](https://jsfiddle.net/IcaroColtec/3frzrdLp/)

####Definir tabelas mais específicas para celulares

Através da classe `.table-sm`.

Exemplo:

```html
<table class="table table-sm">
  <thead>...</thead>
  <tbody>...</tbody>
</table>
```
[Small Table](https://jsfiddle.net/IcaroColtec/yycc2f08/)

####Utilzar tabelas com temas definidos

As tabelas contextuais são um conjunto de classes já definidas pelo bootstrap
cada qual possui um tema. Elas podem ser tanto aplicadas nas lacunas `<tr>` de maneira
individual ou nas células `<td ou th>`.

Alteração feitas nas lacunas:

```html
        <tr class="table-active">...</tr>
        <tr class="table-primary">...</tr>
        <tr class="table-secondary">...</tr>
        <tr class="table-success">...</tr>
        <tr class="table-danger">...</tr>
        <tr class="table-warning">...</tr>
        <tr class="table-info">...</tr>
        <tr class="table-light">...</tr>
        <tr class="table-dark">...</tr>
```

Alterações em campos individuais;

```html
        <td class="table-active">...</td>
        <td class="table-primary">...</td>
        <td class="table-secondary">...</td>
        <td class="table-success">...</td>
        <td class="table-danger">...</td>
        <td class="table-warning">...</td>
        <td class="table-info">...</td>
        <td class="table-light">...</td>
        <td class="table-dark">...</td>
        </tr>
```

[Contextual Tables](https://jsfiddle.net/IcaroColtec/8aofgkmt/)

####Definir descrições para as tabelas criadas

Os capitions são descrições da funcionalidade da tabela criada. 
São declarados logo acima do header através da tag `<caption>`. 

Exemplo:

```html
<table class="table table-sm">
  <caption>Simple</caption>
  <thead>...</thead>
  <tbody>...</tbody>
</table>
```
[Caption](https://jsfiddle.net/IcaroColtec/7Lgqu68t/)

####Dinâmica de Responsividade   

O bootstrap possui uma classe de tabela com layout fluído automático,`.table-responsive`, no entanto os pontos 
de transição entre telas podem ser especificados para adotarem um determinado 
comportamento em um intervalo de dimensões. As dimensões disponibilizadas pela 
framework são:

|Size        | Extra Small     | Small    | Medium      |Large     |Extra Large|
|:----------:| :-------------: |:--------:|:-----------:|:--------:|:---------:|
|**Dimensão**| <576px          | >= 576px | >= 768px    |>= 992px  |>=1200px   |
|**Prefixo** | .col-           |.col-sm   |.col-md      |.col-lg   |.col-xl    |

A definição das dimensões se dá através do uso da class `.table-responsive` seguida
da dimensão a ser especificada.

Exemplo:

```html
        <div class="table-responsive-lg">
                <table class="table">
                ...
                </table>
        </div>
```

##Panels

###Introdução
        
Os paineis são "caixas" que basicamente servem para acomodarem o 
DOM. Assim como as tabelas são sucetíveis à alterações.

####Painel Padrão

Os painéis diferentemente das tabelas são declarados nos containers
padrão, as divs. Sua declaração é feita logo após a tag `<div>` com 
a classe `.panel` juntamente com a `.panel-default`.
Painéis são compostos de header, body e footer, e para serem
instanciados precisam de um container próprio. 
As classes são respectivamente: `.panel-heading`, `panel-body`, `panel-footer`.

Exemplo:
        
```html
        <div class="panel panel-default">
                <div class="panel-heading">Sem Título</div>
                <div class="panel-body">
                <p>Painel Padrão :)</p>
                </div>
                <div class="panel-body">Rodapé aqui!</div>
        </div>
```
    
####Painéis Contextualizados

Possuem temas e cores determinadas:

```html
<div class="panel panel-primary">...</div>
<div class="panel panel-success">...</div>
<div class="panel panel-info">...</div>
<div class="panel panel-warning">...</div>
<div class="panel panel-danger">...</div>
```

####Painéis e Tabelas agregados

As tabelas podem ser agregadas à painéis de maneira que as tabelas fiquem inseridas nos containers dos painéis. Caso o painel tenha um `body` a tabela vêm logo após o conteúdo do `body`, caso contrário a tabela simplesmente é afixada logo abaixo do `header` da tabela.

####Painéis e Listas

As listas também podem ser inseridas logo após o `body` do painel, o formato das listas é declarado como `.list-group`, e os itens da lista como `.list-group-item`.

Exemplo:

```html
<div class="panel panel-default">
  <div class="panel-heading">COLTEC - UFMG</div>
  <div class="panel-body">
    <p>Incipta Vita Nova!</p>
  </div>

  <ol class="list-group">
    <li class="list-group-item">Quem somos nós</li>
  </ol>
</div>
```

####Wells

Container com o simples aspecto de item selecionado. Possuem o padding e margin padrão assim como as tabelas e painéis vistos anteriormente.São declarados através da classe `.well` dentro do container da div em que serão instânciados. Podem sofrar adaptações na altura do container através da adição da class `.well-sm` ou `.well-lg` após a declaração da classe `.well` inicial. 

```html
   <div class="well ">...</div>     
```

##Exercício

Exercício proposto pelo grupo do Mateus, Guilherme, e Gabriel. O tópico apresentado por eles foi: Tabs, Pills e Tabbed Navigation, no final do slide está o exercício.

[Slide](https://github.com/Veazey/Seminarios-Frameworks-CSS/blob/0467742b81493beb74abcc1f84f74e1edb677350/daw%20-%20tab%20navigation.pdf)