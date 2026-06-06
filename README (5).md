# 🚗 Jogo do Carro — Desvie da Burocracia!

Jogo de captação de leads para o movimento cívico **A Região de Americana Merece Mais**.

Desenvolvido em HTML/CSS/JavaScript puro — um único arquivo, sem dependências externas.

---

## Como funciona

O jogador controla um carro em visão aérea desviando de obstáculos burocráticos. Quanto mais longe chega, maior a pontuação. Ao fim, preenche nome, WhatsApp e localização para registrar o recorde — gerando um lead qualificado para o movimento.

O jogador pode compartilhar um link de desafio com o próprio recorde, convidando amigos a superá-lo.

---

## Estrutura

```
jogocarro.html    ← jogo completo (arquivo único)
README.md
```

---

## Publicação

O arquivo é servido via **Cloudflare Pages** no domínio oficial do movimento.  
Também disponível via **GitHub Pages** para testes e desenvolvimento.

### Ativar GitHub Pages

1. Repositório → **Settings → Pages**
2. Source: `Deploy from a branch`
3. Branch: `main` · Pasta: `/ (root)`
4. Salvar — URL disponível em alguns minutos

---

## Integração com o backend (n8n)

Os leads coletados no jogo são enviados via webhook para o n8n, que:

- Registra o contato no CRM (Google Sheets)
- Dispara mensagem de boas-vindas via WhatsApp

Para ativar, edite o arquivo `jogocarro.html` e substitua:

```js
webhookUrl: null,
```

pela URL do webhook do n8n:

```js
webhookUrl: 'https://campanha360.duckdns.org/webhook/game-lead',
```

---

## Controles

| Dispositivo | Ação |
|-------------|------|
| Teclado | `←` `→` ou `A` `D` |
| Mobile | Toque na metade esquerda/direita da tela |
| Mobile | Swipe para o lado desejado |

---

## Power-ups

| Item | Efeito |
|------|--------|
| ⭐ Estrela | +60 pontos |
| 🛡️ Escudo | Invencibilidade temporária |
| 💨 Vento | Reduz a velocidade |

---

*Movimento cívico A Região de Americana Merece Mais · 2026*
