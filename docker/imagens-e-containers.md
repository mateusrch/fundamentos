# Imagens

- Uma imagem docker é formada por camadas, cada camada tem um id único.
- **Qualquer modificação feita na imagem gera uma nova camada**
Exemplo:
1. primeira camada da imagem
    - rodo um sudo apt <algum pacote>, esse pacote será instalado em uma nova camada.

Tendo isso em mente, a minha imagem se torna **READ-ONLY**(somente leitura).
- No momento em que a imagem é gerada ela é **imutável**
- Então eu posso usar essa imagem de base para gerar outra imagem ou deleta-la.

# Containers
- Quando eu inicio um container ele pega uma imagem que é imutável e cria uma nova camada em cima
- O container nada mais pe do que uma camada **Read-Write**
- Quando o container morre, a sua camada é eliminada, restando assim apenas a imagem docker que é imutável.
