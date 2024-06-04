# File System (FHS)

É o sistema de arquivos que roda em cima da partição, cada partição tem seu FHS.

## Overview dos diretórios

- **/bin/(binários)**: Aqui ficam todos os binários que podem ser executados tanto pelo usuário ROOT quando o usuário NORMAL.

- **/boot/(bootavel)**: Todos os arquivos necessários para iniciar o sistema ficam aqui.

- **/dev/(devices)**: Fica uma abstração em objeto para cada dispositivo do sistema, como HDs, Pendrives, teclados, mouses etc..

- **/etc/(configs)**: Quando se instala uma aplicação como LibOffice, os arquivos de configuração estão dentro do /etc/ .

- **/home/(user)**: Aqui ficam os arquivos do usuário, como downloads, vídeos, fotos, etc...

- **/lib/(bibliotecas)**: Aqui ficam arquivos '.so'

- **/media/(montagem)**: Aqui é criado uma abstração para dispositivos inseridos como Pendrives essé diretório é o ponto de montagem

- **/mnt/**(montagem/temporaria)**: Aqui serão montados dispositivos, porem temporariamente.

- **/opt/(optional)**: Geralmente a instalaão de pacotes externos ficam dentro do OPT.

- **/root/**: Vai armazenar o 'HOME' do root

- **/sbin/(binários do sistema)**: Aqui ficam executáveis para recuperar o sistema por exemplo.

- **/srv/(services)**: Aqui ficam instalados os serviços.

- **/tmp/**: Aqui ficam arquivos temporários

- **/usr/**: Aqui existem abstrações para:
  - /bin/
  - /include/
  - /lib/
  - /sbin/

  São as mesmas coisas dos diretório acima, porem focado no usuário.

- **/var/(variaveis)**: É o diretório que vai conter:
  - /cache/
  - /log/(informações de log do sistema e serviços)
  - /spoll/(relacionado a impresoras)
  - /tmp/(arquivos temporários)
