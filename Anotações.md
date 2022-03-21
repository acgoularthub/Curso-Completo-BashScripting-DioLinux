STDIN - Standard input
STDOUT - Standard output - ">" - 1
STDEER - Standard Error -  - 2

* echo "qualquer coisa" 1> /dev/null (encaminha a saída paddrão para o /dev/null)
* echo "qualquer coisa" 2> /dev/null (caso algo der errado será redirecionado como erro para /dev/null)

* echo "qualquer coisa" &> /dev/null (o "&" serve como 1 e 2, ou seja, erro e saida padrão ao mesmo tempo)
* o "redirecionador" da saída [>] tem dois modos de ser usado: o > envia para o arquivo indicado a seguir e caso já haja algo no arquivo será sobrescrito, já o >> anexa a informação ao final do arquivo existente, caso já haja alguma coisa no arquivo.

* Shebang ou hashbang: é uma linha no script, logo ao topo, que serve para definir o caminho para o interpretador (bash).

```bash
#!/usr/bin/env bash

[script]
```

ou 

```bash
#!/bin/bash

[script]
```

O mais indicado é que seja utilizado a primeira opção para evitar problema de compatibilidade entre os sistemas.

A shebang serve como um recurso para a escolha automática do interpretador que irá executar o programa no momento em que executamos o mesmo com o `./`. Exemplo: `./programa.sh`.

* `echo` ou `printf`?

O comando echo não é portável, o `printf` apresenta um controle muito maior na formatação da saída da string, assim como em várias linguagens de programação.