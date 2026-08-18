
1. Essa afirmação significa que a genealogia das linguagens não deve ser vista como uma sequência em que cada linguagem substitui ou supera a anterior. A árvore mostra ramificações, influências e linguagens que coexistem por diferentes motivos. Por exemplo, Fortran, COBOL e Lisp surgiram para necessidades distintas e continuaram sendo utilizadas mesmo após o surgimento de novas linguagens.

Dois fatores explicam essa influência sem substituição:

Contextos de aplicação distintos: cada linguagem é criada para determinados problemas, como Fortran para computação científica e COBOL para processamento comercial. 
Restrições tecnológicas e institucionais: limitações do hardware, sistemas já existentes e investimentos em determinadas tecnologias podem atrasar  a adoção de novas ideias. 

2. O Plankalkül é relevante porque, mesmo sem ter sido implementado, seu projeto de 1945 apresentava recursos muito avançados para a época, alguns que só apareceriam em outras linguagens décadas depois.
Três recursos antecipados foram:
Estruturas de dados avançadas, como vetores e registros aninhados. 
Tipos numéricos baseados em bits, incluindo conceitos relacionados ao ponto flutuante. 
Asserções, usadas para representar relações que deveriam ser verdadeiras durante a execução. 
As asserções são especialmente importantes porque anteciparam uma prática da engenharia de software moderna: verificar e documentar condições esperadas durante a execução de um programa.

3 - O Short Code, o Speedcoding e os sistemas A-0/A-1/A-2 surgem entre 1949 e 1954 para enfrentar o mesmo problema: programar diretamente em código de máquina era lento, difícil e cheio de erros, e era preciso encontrar uma forma de o programador escrever instruções mais próximas da matemática ou mais compactas, sem lidar manualmente com endereços e códigos binários. A diferença entre eles está na estratégia usada para resolver isso.

O Short Code, criado por Mauchly, e o Speedcoding, criado por Backus, adotam a mesma lógica: a interpretação. O programador escrevia instruções em uma notação simplificada, e um programa interpretador lia e traduzia cada instrução no momento em que ela era executada, repetindo essa tradução toda vez que a instrução era alcançada.

Já os sistemas A-0, A-1 e A-2, desenvolvidos por Grace Hopper, seguem outro caminho: em vez de interpretar, eles montam um programa executável a partir de sub-rotinas prontas. O programador indicava uma sequência de códigos numéricos que apontavam para rotinas já escritas em uma biblioteca (como funções matemáticas ou de entrada e saída), e o sistema copiava essas rotinas para a memória, ajustava os endereços e gerava um código de máquina completo, pronto para ser executado quantas vezes fosse necessário. 

4 - Por isso, para que o Fortran fosse adotado, não bastava facilitar a escrita do programa: era preciso provar que o código gerado pelo compilador rodava tão rápido quanto o código feito manualmente por um bom programador, senão ninguém trocaria seu método testado por uma linguagem nova. Por isso a equipe de Backus investiu pesado em otimização do compilador, e não só na tradução da linguagem.

5 - Quanto aos domínios, o Fortran é voltado para cálculos científicos e numéricos e o Lisp é para inteligência artificial. A representação de dados de ambos são dististas o Fortran trabalha com array numéricos de tamanho fixo e o outro trabalha com listas ligadas (listas dinâmicas e con cells, que são basicamente uma estrutura de dados, onde guarda um valor e uma referência para o "restante" da lista). O estilo de computação do Lisp é funcional, ou seja, é composto de funções que retornas valores e recurção no lugar de laços, diferentemente do Fortran, que é uma linguagem imperativa que é executada com uma sequência de comandos.


11. O Algol base da programação estruturada, com construções em blocos, tipagem estático e uso de if, while, for. O Pascal herda estrutura de Algol, é mais didático e disciplina rígida de tipos, já a linguagem C também herda de Algol, porém sua programação é mais voltada para sistemas, com ponteiros e controle de baixo nível, o Prolog por sua vez é diferente: o programador não escreve comandos, apenas fatos e regras, e o próprio sistema busca a resposta sozinho. Não há laços nem variáveis sendo alteradas, a pergunta central é "o que é verdade?", e não "como fazer?".

12. Base Prolog

Fatos:

pai(joao, maria).
pai(joao, pedro).

- (João é pai de Maria. João é pai de Pedro.)

Regra:

irmãos(X, Y) :- pai(Z, X), pai(Z, Y), X \= Y.

(X e Y são irmãos se existe um Z que é pai de X e também pai de Y, e X é diferente de Y.)

Consulta: 

?- irmãos(maria, pedro).

Resposta do sistema: true. O motor de inferência encontra que joao é pai de ambos e que maria ≠ pedro, satisfazendo a regra.

Se fosse só armazenamento (como um banco de dados), os fatos (pai(joao, maria), pai(joao, pedro)) seriam tudo o que existe — registros estáticos, consultados diretamente.

O que torna isso programação lógica é a regra (irmãos): ela não guarda um dado pronto, mas define uma relação derivada, calculada dinamicamente a partir de outros fatos, no momento da consulta. O sistema não "procura" um valor armazenado chamado irmãos(maria, pedro) — ele infere logicamente essa verdade combinando fatos existentes segundo a regra.

15. Java foi criada inicialmente para sistemas embarcados, mas características como portabilidade, segurança e independência de plataforma se tornaram muito úteis com o crescimento da Web. Isso mostra que mudanças tecnológicas podem fazer uma linguagem ser adotada em áreas diferentes daquelas para as quais foi originalmente criada.

18. XSLT recebe documentos XML e aplica regras de transformação para gerar XML, HTML ou texto. JSP processa páginas no servidor, combinando HTML com recursos de Java para gerar conteúdo Web dinâmico. Ambas são híbridas porque misturam elementos de marcação com recursos de programação e processamento.

20. Para cálculo científico, Fortran é adequado por ter sido criado com foco em computação numérica. Para regras declarativas, Prolog é apropriado por trabalhar com fatos e regras lógicas. Para aplicações Web interativas, JavaScript se destaca por ter surgido para adicionar comportamento às páginas Web. Para firmware restrito, C é indicado por sua eficiência e proximidade com o hardware. Os principais trade-offs são abstração versus controle do hardware e facilidade de desenvolvimento versus eficiência de execução.



