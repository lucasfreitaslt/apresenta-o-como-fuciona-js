---
marp: true
lang: en-US
title: Como funciona o Javascript
description: Uma rapida explicação como o javascript é executado
theme: uncover
transition: fade
paginate: true
_paginate: false
---

# Como funciona o
## <!-- fit --> javascript 
## nos bastidores

> por Lucas Freitas

---


#  COMO EXECUTAR JAVASCRIPT 

![bg right:20%](https://fakeimg.pl/800x600/fff/000/?text=?) 


<!-- 
- Todo código JavaScript precisa ser hospedado e executado em *algum* tipo de ambiente. Na maioria dos casos, esse ambiente seria um navegador **web**. 
-->

---

> JAVASCRIPT no

# <!-- fit --> Navegador
![bg opacity:.25](https://d0.momapix.com/gilardi/32000f5fbf3342937b6f0945d2891fd9e3f217f9ff52c1867baa0929bdda7a30eccc5/Preview11990.jpg)

<!-- 
  Entender o conceito de execução do javascript é essesncial para escrever codigos eficientes e livres de erros. Isso nos ajudará a entender escopo, hoisting, a palavra `this` entre outros conceitos importantes da linguagem.

  Nessa apresentação iremos navegar até as profundezas dos navegadores para desconbrir como  o javascript funciona.
-->

---


#  Conceitos 
![w:400](https://fakeimg.pl/800x600/fff/000/?text=🗂️)


![bg vertical left:23%](https://fakeimg.pl/800x600/fff/000/?text=🤓%20%20Parser)
![bg](https://fakeimg.pl/800x600/ddd/000/?text=🛥️%20%20Motor)
![bg](https://fakeimg.pl/800x600/bbb/000/?text=📃%20%20Context)



---


# <!-- fit--> Parser

![alt text](image-5.png)

![bg vertical left:23%](https://fakeimg.pl/800x600/fff/000/?text=🤓%20%20Parser)
![bg opacity:.2](https://fakeimg.pl/800x600/ddd/000/?text=🛥️%20%20Motor)
![bg opacity:.2](https://fakeimg.pl/800x600/bbb/000/?text=📃%20%20Context)

<!-- 

o Parser ou Analisador

é um programa que lê o programa, linha-por-linha. Entende como o codigo se encaixa com a sintaxe que foi definida pela linguagem de programação e o que é esperado que o codigo faça;
-->

___


# <!-- fit--> Motor

<p>

  <img src="image.png" width="150" />
  <img src="image-1.png" width="200" />
  <img src="image-4.png" width="150" />

</p>


![bg vertical left:23% opacity:.2](https://fakeimg.pl/800x600/ddd/000/?text=🤓%20%20Parser)
![bg](https://fakeimg.pl/800x600/fff/000/?text=🛥️%20%20Motor)
![bg opacity:.2](https://fakeimg.pl/800x600/bbb/000/?text=📃%20%20Context)

<!-- 

o Motor

cada navegadores possui um mecanismo. Como por exemplo: o **mecanismo V8** para Google Chrome, **SpiderMonkey** para Firefox e **Chakra** para Internet Explorer. Mas todos eles seguem um padrão que e o **ECMAScript**. Padrão esse que garante que o mesmo codigo poderá ser executado em diferentes motores!

-->

___



# <!-- fit--> Context

```
1. o código específico é analisado 
2. as variáveis e funções são armazenadas na memória 
3. o código de bytes executável é gerado 
4. e finalmente executado,
```

![bg vertical left:23% opacity:.2](https://fakeimg.pl/800x600/ddd/000/?text=🤓%20%20Parser)
![bg opacity:.2](https://fakeimg.pl/800x600/bbb/000/?text=🛥️%20%20Motor)
![bg](https://fakeimg.pl/800x600/fff/000/?text=📃%20%20Context)

<!-- 

o Contexto


- Durante o tempo de execução o Contexto de Execução segue os seguintes passos:

1. o código específico é analisado, 
2. as variáveis e funções são armazenadas na memória, 
3. o código de bytes executável é gerado e 
4. e finalmente executado,



-->

___


# GEC e FEC
## (global e função)


![bg vertical left:23%](https://fakeimg.pl/800x600/ddd/000/?text=%20)
![bg](https://fakeimg.pl/800x600/bbb/000/?text=%20)
![bg](https://fakeimg.pl/800x600/fff/000/?text=📃%20%20Context)

<!--

Exitem dois tipos de "analizadores": GEC e FEC

- O Contexto de Execução Global (GEC) e o Contexto de Execução de Função (FEC) são fundamentais para a estruturação e execução do código JavaScript. O GEC é único e global, enquanto o FEC é criado e destruído cada vez que uma função é chamada. Compreender essas diferenças é crucial para escrever e depurar código JavaScript de forma eficaz.

-->

---

# GEC

![bg right:70% contain](image-6.png)

<!-- 

Sempre que o mecanismo JavaScript recebe um arquivo de script, ele primeiro cria um Contexto de Execução padrão conhecido como Contexto de Execução Global (GEC).

O GEC é o contexto de execução base/padrão onde todo o código JavaScript que não está dentro de uma função é executado.

Para cada arquivo JavaScript, só pode haver um GEC.
-->

---

# FEC

![bg right:70% contain ](image-8.png)


<!-- 

Sempre que uma função é chamada, o mecanismo JavaScript cria um tipo diferente de Contexto de Execução conhecido como Contexto de Execução de Função (FEC) dentro do GEC para avaliar e executar o código dentro dessa função.

Como cada chamada de função recebe seu próprio FEC, pode haver mais de um FEC no tempo de execução de um script.

-->
---

# Fases 
### do Contexto de Execução

- Fase de Criação
- Fase de  Execução 

---

# Fase de
### Criação 


1. Criação um Objeto Variavel (VO)
2. Criação da cadeia de Escopo (Scope Chain)
3. Determina o Valor do `this`

---

# VO 
## Hosting

![bg vertical right:60% contain](image-9.png)
![bg vertical contain](image-10.png)

<!-- 

  
-->

---


<!-- 


 **Criação do Objeto Variável (VO)**
 - Objeto Variável (VO): E um conceito abstrato que representa o armazenamento de variáveis, declarações de função e parâmetros de função dentro de um contexto de execução.

**topico 3**

**Fases de Criação do Contexto de Execução**

1. **fase de criação**
 - Durante esta fase, o mecanismo JavaScript executa as seguintes etapas:
  
*  Cria o objeto variável.
*  configura a cadeia de escopo.
* Determina o valor de "**this**"
* declarações *Hoists* e declarações de variáveis.
- **elevação:**

* As declarações de função são adicionadas ao Objeto Variável com suas definições.
* As declarações de variáveis são adicionadas ao Objeto Variável com um valor inicial de undefined.
2. **fase de execução:**
- O mecanismo JavaScript executa o código linha por linha.
* As variáveis recebem valores e as funções são executadas à medida que o código é executado.
- exemplo:

![image](https://hackmd.io/_uploads/Sk2PbIMEA.png)


-->


