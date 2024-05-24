## apresentação como fuciona js 

**TOPICO 1**
  1. COMO EXECUTAR JAVASRIPT?: 
- Todo código JavaScript precisa ser hospedado e executado em *algum* tipo de ambiente. Na maioria dos casos, esse ambiente seria um navegador **web**.
- **o navegador não entende nativamente o código JavaScript** de alto nível que escrevemos em nossos aplicativos. Ele precisa ser convertido em um formato que o navegador e nossos computadores possam entender – código de máquina. Com base nisso os navegadores precisa de um programa de computador que recebe o código-fonte JavaScript e o compila nas instruções binárias (código de máquina) que uma CPU pode entender. 
- cada navegadores possui um mecanismo Os exemplos: o **mecanismo V8** para Google Chrome, **SpiderMonkey** para Firefox e **Chakra** para Internet Explorer. Mas todos eles seguem um padrão que e o **ECMAScript**.
- Durante o tempo de execução do Contexto de Execução, o código específico é analisado por um analisador, as variáveis e funções são armazenadas na memória, o código de bytes executável é gerado e o código é executado, exitem dois tipos de "analizadores", **Contexto de Execução Global** (GEC), **Contexto de execução de função** (FEC).

**topico 2**
- O Contexto de Execução Global (GEC) e o Contexto de Execução de Função (FEC) são fundamentais para a estruturação e execução do código JavaScript. O GEC é único e global, enquanto o FEC é criado e destruído cada vez que uma função é chamada. Compreender essas diferenças é crucial para escrever e depurar código JavaScript de forma eficaz.
- exemplo de codigo (**GEC**):

![image](https://hackmd.io/_uploads/HJN3k70mR.png)
- exemplo de codigo (**FEC**):
![image](https://hackmd.io/_uploads/r1stW7CXC.png)



