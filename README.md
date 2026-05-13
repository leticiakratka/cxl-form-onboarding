# Caixa Livre · Diagnóstico

Formulário de onboarding para alunos do Caixa Livre. Triagem em 7 etapas com lógica de redirect por persona + renda.

## Estrutura

- `index.html` — formulário (publicar como página estática)
- `logo-lck.png` — logo no header
- `apps-script.gs` — código pra colar em Extensões → Apps Script da planilha de onboarding

## Fluxo

1. Lead preenche 7 etapas
2. Apps Script grava na planilha + dispara webhook pro n8n
3. Tela final adapta por persona detectada (Milena vs Ana Luiza) + renda + interesse
   - Renda >7k + interesse sim/talvez → call gratuita com Vanessa
   - Renda ≤7k + interesse sim/talvez → WhatsApp Jeane
   - Não → agradecimento sem CTA

## Atualizar

Pra editar o `index.html`, basta editar e fazer commit + push. Pra editar o Apps Script, precisa criar **nova implantação** (não editar a existente) no Google Apps Script.
