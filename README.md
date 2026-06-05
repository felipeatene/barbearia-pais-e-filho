# barbearia-pais-e-filho

Landing page completa da **Barbearia Pais e Filhos** — um conceito de bar +
barbearia. Site estático (HTML + Tailwind via CDN) com design escuro, animações
de scroll e modal de agendamento integrado via WhatsApp.

## Estrutura do site

| Seção | Descrição |
|---|---|
| **Hero** | Primeira impressão com frase de impacto e CTA de agendamento |
| **A Vibe** | Conceito do espaço: a cadeira, o balcão e a tradição |
| **Serviços** | Bloco A (cortes/barba) e Bloco B (drinks/petiscos) |
| **Galeria** | Vitrine do ambiente com placeholders para as fotos reais |
| **Fidelidade** | Programa de retorno por visitas com CTA de cadastro |
| **Footer** | Endereço, horários, WhatsApp e Instagram |

O **agendamento** acontece num modal de 3 passos (serviço → dia → horário)
que abre ao clicar em qualquer botão "Agendar". Ao confirmar, o cliente é
redirecionado ao WhatsApp da barbearia com a mensagem formatada.

## Como usar localmente

Por ser um site estático, basta abrir o `index.html` no navegador. Para evitar
restrições de alguns navegadores, sirva localmente:

```bash
python3 -m http.server 8000
# acesse http://localhost:8000
```

## Configuração

As configurações ficam no topo do `<script>` em `index.html`:

| Variável | Descrição |
|---|---|
| `WHATSAPP_NUMBER` | Número da barbearia no formato internacional (somente dígitos: DDI + DDD + número). **Substitua pelo número real.** |
| `SCHEDULE_YEAR` | Ano exibido no calendário de agendamento. |
| `SCHEDULE_MONTH` | Mês exibido no calendário (`0` = Janeiro … `11` = Dezembro). O calendário calcula automaticamente o primeiro dia e o total de dias do mês. |

Além das variáveis JS, lembre de atualizar diretamente no HTML:
- Endereço completo no **Footer** (`📍 Rua Exemplo…`)
- Link do **Instagram** no Footer
- Link de cadastro no **Clube de Fidelidade**

### Adicionando fotos reais à Galeria

Substitua os `<div>` com gradiente dentro de `renderGallery()` por `<img>`
apontando para as fotos reais do espaço.

## Deploy automático (GitHub Pages)

O repositório inclui o workflow `.github/workflows/deploy-pages.yml`, que
publica o site no GitHub Pages a cada `push` na branch `main`.

Para ativar, em **Settings → Pages**, selecione **Source: GitHub Actions**.
