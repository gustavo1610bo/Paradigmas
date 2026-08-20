
# História das Linguagens de Programação

### Atividade Acadêmica — Genealogia, Paradigmas e Evolução das Linguagens

---

## Questão 1 — Genealogia sem substituição

Essa afirmação significa que a genealogia das linguagens não deve ser vista como uma sequência em que cada linguagem substitui ou supera a anterior. A árvore genealógica mostra ramificações, influências e linguagens que **coexistem** por diferentes motivos. Fortran, COBOL e Lisp, por exemplo, surgiram para atender necessidades distintas e continuaram sendo utilizadas mesmo após o surgimento de novas linguagens.

**Dois fatores explicam essa influência sem substituição:**

| Fator | Explicação |

|---|---|

| **Contextos de aplicação distintos** | Cada linguagem é criada para determinados problemas — como Fortran para computação científica e COBOL para processamento comercial. |

| **Restrições tecnológicas e institucionais** | Limitações de hardware, sistemas já existentes e investimentos em determinadas tecnologias podem atrasar a adoção de novas ideias. |

---

## Questão 2 — O Plankalkül e seus recursos à frente do tempo

O Plankalkül é relevante porque, mesmo sem ter sido implementado, seu projeto de 1945 apresentava recursos muito avançados para a época — alguns que só apareceriam em outras linguagens décadas depois.

**Três recursos antecipados:**

1. **Estruturas de dados avançadas**, como vetores e registros aninhados.

2. **Tipos numéricos baseados em bits**, incluindo conceitos relacionados a ponto flutuante.

3. **Asserções**, usadas para representar relações que deveriam ser verdadeiras durante a execução.

As asserções são especialmente importantes porque anteciparam uma prática da engenharia de software moderna: **verificar e documentar condições esperadas durante a execução de um programa.**

---

## Questão 3 — Short Code, Speedcoding e os sistemas A-0/A-1/A-2

O Short Code, o Speedcoding e os sistemas A-0/A-1/A-2 surgem entre 1949 e 1954 para enfrentar o mesmo problema: programar diretamente em código de máquina era lento, difícil e cheio de erros. Era preciso encontrar uma forma de o programador escrever instruções mais próximas da matemática ou mais compactas, sem lidar manualmente com endereços e códigos binários. A diferença entre eles está na **estratégia usada para resolver isso**.

### Interpretação — Short Code e Speedcoding

O **Short Code** (criado por Mauchly) e o **Speedcoding** (criado por Backus) adotam a mesma lógica: a interpretação. O programador escrevia instruções em uma notação simplificada, e um programa interpretador lia e traduzia cada instrução no momento em que ela era executada, repetindo essa tradução toda vez que a instrução era alcançada.

### Montagem por sub-rotinas — A-0, A-1 e A-2

Já os sistemas **A-0, A-1 e A-2**, desenvolvidos por Grace Hopper, seguem outro caminho: em vez de interpretar, eles montam um programa executável a partir de sub-rotinas prontas. O programador indicava uma sequência de códigos numéricos que apontavam para rotinas já escritas em uma biblioteca (como funções matemáticas ou de entrada e saída), e o sistema copiava essas rotinas para a memória, ajustava os endereços e gerava um código de máquina completo — pronto para ser executado quantas vezes fosse necessário.

---

## Questão 4 — O desafio da adoção do Fortran

Para que o Fortran fosse adotado, não bastava facilitar a escrita do programa: era preciso provar que o código gerado pelo compilador rodava **tão rápido quanto** o código feito manualmente por um bom programador. Caso contrário, ninguém trocaria seu método já testado por uma linguagem nova.

Por esse motivo, a equipe de Backus investiu pesado em **otimização do compilador**, e não apenas na tradução da linguagem.

---

## Questão 5 — Fortran x Lisp

| Aspecto | Fortran | Lisp |

|---|---|---|

| **Domínio** | Cálculos científicos e numéricos | Inteligência artificial |

| **Representação de dados** | Arrays numéricos de tamanho fixo | Listas ligadas (dinâmicas), compostas por *cons cells* — estrutura que guarda um valor e uma referência para o "restante" da lista |

| **Estilo de computação** | Imperativo — sequência de comandos executados em ordem | Funcional — composto por funções que retornam valores, usando recursão no lugar de laços |

---

## Questão 11 — Descendentes do Algol

O **Algol** é a base da programação estruturada, com construções em blocos, tipagem estática e uso de if, while, for.

- **Pascal** herda a estrutura do Algol: é mais didático e possui disciplina rígida de tipos.

- **C** também herda do Algol, porém sua programação é mais voltada para sistemas, com ponteiros e controle de baixo nível.

- **Prolog** é radicalmente diferente: o programador não escreve comandos, apenas **fatos e regras**, e o próprio sistema busca a resposta sozinho. Não há laços nem variáveis sendo alteradas — a pergunta central é *"o que é verdade?"*, e não *"como fazer?"*.

---

## Questão 12 — Programação lógica em Prolog

**Fatos:**

pai(joao, maria).

pai(joao, pedro).
*(João é pai de Maria. João é pai de Pedro.)*

**Regra:**

irmãos(X, Y) :- pai(Z, X), pai(Z, Y), X \\= Y.
*(X e Y são irmãos se existe um Z que é pai de X e também pai de Y, e X é diferente de Y.)*

**Consulta:**

?- irmãos(maria, pedro).
**Resposta do sistema:** true. O motor de inferência encontra que joao é pai de ambos e que maria ≠ pedro, satisfazendo a regra.

### Por que isso é programação lógica, e não apenas armazenamento?

Se fosse só armazenamento (como um banco de dados), os fatos (pai(joao, maria), pai(joao, pedro)) seriam tudo o que existe — registros estáticos, consultados diretamente.

O que torna isso **programação lógica** é a regra irmãos: ela não guarda um dado pronto, mas define uma **relação derivada**, calculada dinamicamente a partir de outros fatos, no momento da consulta. O sistema não "procura" um valor armazenado chamado irmãos(maria, pedro) — ele **infere logicamente** essa verdade combinando fatos existentes segundo a regra.

---

## Questão 15 — Java e a reinvenção de propósito

Java foi criada inicialmente para **sistemas embarcados**, mas características como portabilidade, segurança e independência de plataforma se tornaram muito úteis com o crescimento da Web.

Isso mostra que mudanças tecnológicas podem fazer uma linguagem ser adotada em áreas diferentes daquelas para as quais foi originalmente criada.

---

## Questão 18 — XSLT e JSP: linguagens híbridas

- **XSLT** recebe documentos XML e aplica regras de transformação para gerar XML, HTML ou texto.

- **JSP** processa páginas no servidor, combinando HTML com recursos de Java para gerar conteúdo Web dinâmico.

Ambas são consideradas **híbridas** porque misturam elementos de marcação com recursos de programação e processamento.

---

## Questão 20 — Linguagem certa para o domínio certo

| Domínio | Linguagem indicada | Justificativa |

|---|---|---|

| Cálculo científico | **Fortran** | Criado com foco em computação numérica |

| Regras declarativas | **Prolog** | Trabalha com fatos e regras lógicas |

| Aplicações Web interativas | **JavaScript** | Surgiu para adicionar comportamento às páginas Web |

| Firmware restrito | **C** | Eficiência e proximidade com o hardware |

**Principais trade-offs:**

- Abstração **versus** controle do hardware

- Facilidade de desenvolvimento **versus** eficiência de execução

---

*Documento organizado a partir das respostas da atividade de História das Linguagens de Programação.*
