# Sessões do bash

- login shell(via ssh por exemplo)
- shell interativo: onde ue posso enviar comandos e ver algum output
- shell não interativo(usado em scrips)

## Ordem de execução dos arquivos

Quando o shell for invocado ele irá porcurar algum desses arquivos listados abaixo,
o primeiro arquivo que ele encontrar será executado. Apenas 1 arquivo é executado.

## Arquivos de configuração system-wide(globais)
- /etc/bash.bash
  > É lido por todos os shells bash, ele define variáveis globais e alias que todos os usuários podem acessar
- /etc/bash.profile
  > é lido por todos os shelss Bourne e compátives, também define variávis e alias que todo os usuários acessam

## Arquivos de configuração do usuário
- ~/.bashrc (define variáveis e alias específicos do usuário)
- ~/.bash_profile (define variáveis e alias específicos do usuário)
- ~/.bash_login (utilizado para iniciar um nova sessão)

Sub shells herdam as variáveis de ambiente de seus shells pais.
