# Barbearia Pais e Filho

Projeto de página única (HTML) para simular o fluxo de agendamento da barbearia.

## Visão geral

Este projeto apresenta uma interface simples e responsiva com 3 etapas:

1. Seleção de serviço  
2. Seleção de dia  
3. Seleção de horário

Ao final, o agendamento é confirmado e o formulário é reiniciado.

## Estrutura do projeto

```text
barbearia-pais-e-filho/
├── index.html   # Página principal com HTML, estilos e lógica JavaScript
└── README.md    # Documentação e organização do projeto
```

## Como executar

Como é um projeto estático, basta abrir o arquivo abaixo no navegador:

- `/tmp/workspace/felipeatene/barbearia-pais-e-filho/index.html`

Opcionalmente, você pode usar uma extensão de servidor local (ex.: Live Server) para facilitar o desenvolvimento.

## Tecnologias usadas

- HTML5
- Tailwind CSS (CDN)
- Animate.css (CDN)
- JavaScript puro (Vanilla JS)

## Organização interna do `index.html`

- **Cabeçalho (`<head>`)**
  - Metadados da página
  - Importação de Tailwind, Animate.css e fonte Inter
  - Estilos customizados (scrollbar, classes auxiliares e toast)
- **Corpo (`<body>`)**
  - Card de apresentação da barbearia
  - Card principal com fluxo em etapas (`step-1`, `step-2`, `step-3`)
  - Botões de navegação (`Avançar` e `Trocar dia/serviço`)
  - Componente de feedback (`toast`)
- **Script**
  - Dados mockados (`services` e `times`)
  - Estado da aplicação (`currentStep`, seleção de serviço, dia e horário)
  - Funções de renderização (`renderServices`, `renderCalendar`, `renderTimes`)
  - Controle de navegação (`nextStep`, `prevStep`, `updateView`)
  - Feedback de validação (`showToast`)

## Objetivo da estrutura

A estrutura foi organizada para que qualquer pessoa consiga:

- entender rapidamente o que o projeto faz;
- localizar os arquivos principais;
- identificar onde está cada parte da interface e da lógica.