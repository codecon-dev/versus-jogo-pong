# Pong Multiplayer 🏓

> *Jogo de Pong multiplayer no navegador com partidas em tempo real.*

## Sobre o Projeto

Pong multiplayer jogável direto no navegador. Dois jogadores se conectam, cada um no seu computador, e jogam uma partida de Pong em tempo real.

O projeto foi criado durante um desafio ao vivo no canal da [Codecon](https://youtube.com/codecondev), onde uma dupla de front-end + back-end competiu contra um dev full-stack solo para ver quem entregava o melhor Pong multiplayer em 4 horas.

## Funcionalidades

- **Multiplayer em tempo real** — Dois jogadores conectados via WebSocket, cada um no seu navegador
- **Game loop sincronizado** — Estado do jogo gerenciado no servidor para evitar dessincronização
- **Power-up de velocidade** — Um ícone aparece na tela e, ao ser atingido pela bolinha, ela acelera
- **Renderização no navegador** — Toda a parte visual roda no client-side

## Arquitetura

```
┌─────────────────┐      ┌─────────────────┐
│                 │      │                 │
│    Client       │◄────►│    Server       │
│  (Navegador)    │  WS  │  (Game Logic)   │
│                 │      │                 │
└─────────────────┘      └─────────────────┘
        │                        │
   Renderização            Game loop
   Input do jogador        Sincronização
   UI                      Colisões
```

- **Client**: Captura input do jogador, renderiza o estado do jogo recebido do servidor
- **Server**: Gerencia o game loop, calcula colisões, sincroniza o estado entre os dois jogadores via WebSocket

## Participe Você Também!

**Acha que consegue fazer melhor?** Mostre suas habilidades!

### Como Contribuir

1. **Fork** este repositório
2. Crie uma pasta com seu nome/username
3. Desenvolva seu sistema de autenticação
4. Documente seu processo no README
5. Abra um **Pull Request**

### Template de Documentação

Seu README deve incluir:
- **Stack**: Tecnologias do projeto
- **Abordagem de Segurança**: Como protegeu as senhas e sessões?
- **Resultado**: Screenshots ou demo
- **Aprendizados**: O que funcionou? O que mudaria?

## 🤝 Apoie a Codecon

Gostou do desafio? Apoie a criação de mais conteúdos como este!

### Codecon PRO - Apenas R$ 15/mês
- 🎫 Crachá especial na Codecon Summit
- 💬 Acesso ao grupo secreto no WhatsApp/Discord
- 🎬 Acompanhe os bastidores dos eventos
- 📧 Newsletter semanal exclusiva
- 🎨 Tema da Codecon para VSCode

[Assine agora em codecon.dev/pro](https://codecon.dev/pro)

## 📱 Siga a Codecon

- [Instagram](https://instagram.com/codecondev) - @codecondev
- [YouTube](https://youtube.com/codecondev) - Vídeos toda semana
- [Site Oficial](https://codecon.dev) - Todos os eventos

## 📜 Licença

Este projeto está sob licença MIT. Sinta-se livre para explorar, aprender e compartilhar!

---

*Feito com ⌨️ e muita raça pela comunidade Codecon*

**#Hacklab #Autenticação #Codecon #SeniorVsJunior**
