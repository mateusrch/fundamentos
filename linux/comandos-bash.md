# Comando 'cp'

## Flags
- '-a' que representa:
  - recurssividade
  - mantem os links
  - preserva as permissões

- '-u' que representa(interessante ao fazer um backup pois copia apenas as mudanças):
  - update
  - consigo copiar apenas os arquivos que ocorreram mudanças.

- '-p' que representa:
- preservar permissões, grupos, links, etc...

Sempre que eu uso o 'cp' *sem nenhuma flag*, ele **altera todas** as informações do item
copiado, desfaz os links, muda as permissões, etc...
<br>

# Comando 'touch'

## Flags
- '-a': atualiza apenas o tempo de acesso
- '-m': atualiza apenas o tempo de modificação
- '-d': especifica uma data e hora pespecíficas para os timestamps.
- '-r': user os timestamps de putro arquivo como referência para atualizar os timestamps do arquivo atual


A Real função do comando 'touch' é atualizar os timestamps de arquivos existentes para o tempo atual,
mas ele também serve para criar arquivos caso eles não existam.

Atributos que são modificados:
- **Acesso(atime - access time)**: indica quando oarquivo foi acessado
- **Modificação(mtime - modification time)**: indica quando o arquivo foi modificado pela última vez
- **Mudança(ctime - change time)**: indica quandos os metadados do arquivo foram modificados(owner, grupo owner)

# Comando 'stat'

## Flags
- '-L': faz com que o 'stat' siga o link simbólico e mostre informações sobre o arquivo alvo.
- '-c': formata o output, eu escolho quais e em que ordem serão exibidas
  > '%n': nome do arquivo
  > '%s': tamanho do arquivo em bytes
  > '%y': ultima data e hora de modificação
  > '%a': permissões do arquivo em formato numérico(755)
  > '%A': permissões em formato de texto(rwxr-xr-x)
  > '%G': nome do grupo do arquivo

O comando 'stat' é usado para exibir informações detalhadas sobre arquivos ou diretórios.
