# Comandos

- **docker run(docker container run)<container>:<tag>**: roda um container, trava o terminal no container
- **docker run -d <container>:<tag>**: Roda um container, trava o terminal no container
- **docker ps**: Lista os containers que estão rodando
- **docker ps -a**: Lista todos os contêiners
- **docker container stop<conteiner-id>**: dropa o contêiner
- **docker container top <conteiner-id>**: mostra os processos dentro do conteiner
- **docker container stats <conteiner-id>**: mostra consumo de cpu, memoria etc...

### Redirecionar portas
- docker run -d -p <portaHost:portaContêiner> <container>:<tag>
- docker run -d -P <container>:<tag>

-d = detach
-p = port
-P = porta randomica
-f ler logs em tempo real

### Logs
- docker logs <conteier-id> -f

**Detach** siginifica sair do modo terminal conectado a um contêiner sem interromper a execução do contêiner.
**Attach** significa se conectar ao terminal atual a um container em execução
