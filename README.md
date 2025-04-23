# Phasmo Helper Data

Repositório de dados abertos para o projeto [Phasmo Helper](https://github.com/hhs0001/phasmo-helper).

## 📋 Sobre o Repositório

Este repositório contém os dados estruturados de fantasmas, evidências e comportamentos utilizados pelo Phasmo Helper. O objetivo é centralizar e facilitar a atualização das informações do jogo Phasmophobia, permitindo que a comunidade contribua e mantenha os dados sempre atualizados.

## 📁 Estrutura dos Dados

- `ghosts/` — Diretório contendo arquivos JSON com os dados de cada fantasma, organizados por idioma (ex: `pt-br.json`).
- Cada arquivo segue um schema padronizado, garantindo consistência e fácil integração com o app principal.

## 🗂️ Exemplo de Estrutura de Dados

```json
{
    "id": "spirit",
    "name": "Espírito",
    "description": "O Espírito é o fantasma mais comum, geralmente pacífico, mas perigoso quando irritado. Incensos são muito eficazes contra ele.",
    "evidences": ["EMF", "SpiritBox", "GhostWriting"],
    "guaranteedEvidences": [],
    "strengths": "Nenhuma força específica aparente.",
    "weaknesses": "Incensos impedem caça por 180s (normal: 90s).",
    "behaviors": [
      {
        "description": "Após ser incensado, espera 180s para caçar novamente (normal: 90s)."
      }
    ],
    "huntThreshold": 50,
    "speedRange": {
      "min": 1.7,
      "max": 1.7
    },
    "hasLOS": true,
    "speedDetails": {
      "baseSpeed": 1.7,
      "description": "Velocidade normal (1.7 m/s)",
      "variableSpeed": false
    }
  },
  // ... outros fantasmas ...
```

## 📝 Schema dos Dados

Os arquivos JSON seguem o seguinte schema (resumido):
- `id`: string — Identificador único do fantasma
- `name`: string — Nome do fantasma
- `description`: string — Descrição
- `evidences`: array — Evidências possíveis
- `guaranteedEvidences`: array (opcional) — Evidências garantidas
- `strengths`: string — Pontos fortes
- `weaknesses`: string — Pontos fracos
- `behaviors`: array — Comportamentos especiais
- `huntThreshold`: number — % de sanidade para caçada
- `speedRange`: objeto `{ min, max }` — Velocidade em m/s
- `hasLOS`: boolean — Se acelera com linha de visão
- `speedDetails`: objeto — Detalhes de velocidade
- `media`: array (opcional) — Mídias relacionadas

Para detalhes completos, consulte o arquivo [`ghost-schema.ts`](https://github.com/hhs0001/phasmo-helper/blob/main/src/types/ghost-schema.ts) no projeto principal.

## 🤝 Como Contribuir

1. Faça um fork deste repositório
2. Crie uma branch para sua alteração (`git checkout -b update/dados`)
3. Edite ou adicione os arquivos JSON conforme necessário
4. Abra um Pull Request explicando suas mudanças

Contribuições para correção de dados, adição de novos fantasmas ou melhorias são bem-vindas!

## 📄 Licença

Este repositório segue a licença GNU GPL v3.0 — veja o arquivo [LICENSE](./LICENSE) para mais detalhes.

## 📱 Contato

- **Projeto principal:** [hhs0001/phasmo-helper](https://github.com/hhs0001/phasmo-helper)
- Dúvidas ou sugestões? Abra uma issue ou contribua diretamente!

---

<div align="center">
  <p>Dados abertos para a comunidade Phasmophobia</p>
  <p><small>Não afiliado oficialmente ao Phasmophobia ou Kinetic Games</small></p>
  <p><small>© 2025 Phasmo Helper Data. Licença GNU GPL v3.</small></p>
</div>
