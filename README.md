# barbearia-pais-e-filho

Página de agendamento online da **Barbearia Pais e Filhos**. É uma aplicação
estática (HTML + Tailwind via CDN) que guia o cliente em 3 passos: escolher o
serviço, o dia e o horário. Ao confirmar, o agendamento é enviado para o
WhatsApp da barbearia com a mensagem já formatada.

## Como usar localmente

Por ser um site estático, basta abrir o `index.html` no navegador. Para evitar
restrições de alguns navegadores, você pode servir localmente:

```bash
python3 -m http.server 8000
# acesse http://localhost:8000
```

## Configuração

As configurações ficam no topo do `<script>` em `index.html`:

- `WHATSAPP_NUMBER`: número da barbearia no formato internacional (somente
  dígitos: DDI + DDD + número). **Substitua pelo número real.**
- `SCHEDULE_YEAR` / `SCHEDULE_MONTH`: ano e mês exibidos na agenda
  (`SCHEDULE_MONTH` usa 0 = Janeiro ... 11 = Dezembro). O calendário calcula
  automaticamente o dia da semana inicial e o total de dias do mês.

## Deploy automático (GitHub Pages)

O repositório inclui o workflow `.github/workflows/deploy-pages.yml`, que
publica o site no GitHub Pages a cada `push` na branch `main`.

Para ativar, em **Settings → Pages**, selecione **Source: GitHub Actions**.
