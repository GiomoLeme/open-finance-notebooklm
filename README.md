# Open Finance no Brasil com NotebookLM

Projeto de estudo desenvolvido para o **Bootcamp Bradesco - GenAI, Dados & Cyber**, em parceria com a **DIO**, com foco nos fundamentos do Open Finance no Brasil e no uso responsável do NotebookLM para pesquisa baseada em fontes.

> Este é um projeto de documentação e aprendizado. Não contém aplicação, código executável ou dependências de software.

## Sobre o desafio

O desafio propõe a criação de um caderno temático no NotebookLM a partir de fontes abertas. O trabalho reúne curadoria de fontes, perguntas estratégicas, experimentos de engenharia de prompts, respostas fundamentadas, registro de dificuldades, glossário, prompts reutilizáveis e um miniguia de estudo.

## Tema e objetivo

**Tema:** Open Finance no Brasil: compartilhamento de dados, APIs, consentimento, segurança e benefícios.

**Objetivo:** compreender como ocorre o compartilhamento de dados entre instituições, qual é o papel do consentimento e das APIs, quais benefícios podem surgir para consumidores e instituições e quais cuidados de segurança e privacidade são relevantes.

## Fontes utilizadas

### Fontes principais em texto/PDF

1. [Banco Central do Brasil - FAQ Open Finance](https://www.bcb.gov.br/meubc/faqs/s/open-finance)
2. [Serasa - Open Finance é seguro? Riscos, vantagens e cuidados](https://www.serasa.com.br/score/blog/open-finance-e-seguro/)
3. [Banco Central do Brasil - Relatório de Cidadania Financeira 2025 (PDF)](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/RIF/Relatorio_de_Cidadania_Financeira_2025.pdf)
4. [Open Finance Brasil - Área do Desenvolvedor](https://openfinancebrasil.atlassian.net/wiki/spaces/OF/pages/17367092)

### Vídeo complementar

- [Open Finance: a nova era das finanças - Marcos Cavagnoli e Rodrigo Linhares](https://www.youtube.com/watch?v=vAZUJHy7ch8)

## Metodologia

1. Definição do tema, do objetivo e do público iniciante.
2. Seleção de cinco fontes com perspectivas regulatória, educacional, estratégica e técnica.
3. Formulação de nove perguntas estratégicas.
4. Geração de respostas no NotebookLM com base nas fontes fornecidas.
5. Realização de três experimentos A/B com prompts simples e prompts mais restritivos.
6. Comparação das respostas, verificação do suporte documental e registro das limitações.
7. Organização dos aprendizados em documentos temáticos e em um miniguia.

O NotebookLM não foi usado para “treinar um modelo”. Ele foi utilizado para responder e sintetizar conteúdo com base nas fontes adicionadas ao caderno.

## Perguntas estratégicas

O estudo foi guiado por nove questões:

1. O que é Open Finance e qual problema busca resolver?
2. Como funciona o compartilhamento de dados?
3. Quais dados podem ser compartilhados?
4. O que é consentimento e quais controles o cliente possui?
5. Qual é o papel das APIs?
6. Quais mecanismos de segurança e privacidade são apresentados nas fontes?
7. Quais benefícios são apontados para consumidores, instituições e sistema financeiro?
8. Quais riscos, desafios e limitações são mencionados?
9. Em que as fontes convergem e como seus enfoques diferem?

As sínteses e as fontes associadas a cada questão estão em [Perguntas estratégicas](docs/perguntas-estrategicas.md).

## Conteúdo estudado

O Open Finance é apresentado nas fontes como um ecossistema regulado que permite ao cliente autorizar o compartilhamento de dados e o uso de serviços entre instituições participantes. O consentimento delimita os dados, as instituições envolvidas, a finalidade e o prazo. As APIs viabilizam a comunicação padronizada entre os sistemas. Entre os benefícios discutidos estão maior portabilidade das informações, ofertas mais adequadas ao perfil do cliente e gestão financeira consolidada. Entre os cuidados estão a gestão ativa dos consentimentos e a prevenção contra fraudes e engenharia social.

## Engenharia de prompts

Foram comparados três pares de prompts:

| Experimento | Prompt simples | Melhoria introduzida |
| --- | --- | --- |
| Definição de Open Finance | Pergunta ampla | Público-alvo, estrutura da resposta e indicação das fontes |
| APIs | Pergunta técnica aberta | Restrição explícita às evidências disponíveis e separação entre fatos e interpretação |
| Segurança e riscos | Pergunta binária | Separação entre mecanismos do ecossistema, riscos ligados ao tema e riscos gerais da digitalização financeira |

Os prompts originais e as conclusões estão em [Engenharia de prompts](docs/engenharia-de-prompts.md).

### Cicatriz principal: detalhes técnicos sobre APIs

Uma resposta inicial apresentou tecnologias e detalhes de implementação como OAuth 2.0, OpenID Connect, FAPI, mTLS, JWT, endpoints e formatos de payload. Ao receber um prompt mais restritivo, o próprio NotebookLM reconheceu que esses elementos **não estavam explicitamente documentados nas fontes consultadas**.

Esse episódio evidencia quatro práticas importantes:

- aplicar *grounding*, limitando a resposta ao material disponível;
- pedir referências e distinguir fatos de analogias ou interpretações;
- desconfiar de respostas tecnicamente sofisticadas quando a evidência não está visível;
- revisar e validar o conteúdo antes de publicá-lo.

## Materiais

- [Perguntas estratégicas](docs/perguntas-estrategicas.md)
- [Registro das respostas do NotebookLM](docs/registro-respostas-notebooklm.md)
- [Engenharia de prompts](docs/engenharia-de-prompts.md)
- [Glossário](docs/glossario.md)
- [Prompts reutilizáveis](docs/prompts-reutilizaveis.md)
- [Miniguia de Open Finance](docs/miniguia-open-finance.pdf)

## Aprendizados

- Respostas mais úteis surgem quando o prompt define público, formato e critérios de evidência.
- A exigência de fontes melhora a rastreabilidade, mas não substitui a conferência humana.
- Um texto convincente pode conter detalhes não sustentados pelo conjunto de fontes.
- Separar riscos do Open Finance de riscos gerais do ambiente financeiro digital evita generalizações.
- Restrições explícitas ajudam o modelo a reconhecer lacunas em vez de preenchê-las com conhecimento externo.

## Limitações

- O conteúdo reflete apenas as fontes fornecidas ao NotebookLM e o momento em que o caderno foi produzido.
- As respostas geradas podem conter simplificações, interpretações ou afirmações que exigem validação nas fontes originais.
- O miniguia é um artefato gerado no processo, não uma fonte primária.
- Afirmações muito específicas do miniguia, incluindo números exatos, percentuais, “criptografia de ponta a ponta”, exemplos de Pix em aplicativos de mensagens e efeitos absolutos sobre o Serasa Score, não são destacadas neste repositório sem verificação documental adicional.
- O material tem finalidade educacional e não constitui orientação financeira, jurídica ou de segurança.

## Estrutura do repositório

```text
open-finance-notebooklm/
├── README.md
├── docs/
│   ├── perguntas-estrategicas.md
│   ├── registro-respostas-notebooklm.md
│   ├── engenharia-de-prompts.md
│   ├── glossario.md
│   ├── prompts-reutilizaveis.md
│   └── miniguia-open-finance.pdf
```

## Referências

Consulte as cinco fontes listadas em [Fontes utilizadas](#fontes-utilizadas). Para manter a rastreabilidade, as sínteses das perguntas indicam quais fontes foram associadas a cada resposta no caderno.

## Contexto acadêmico

Projeto de bootcamp e portfólio complementar, criado no contexto do **Bootcamp Bradesco - GenAI, Dados & Cyber + DIO**. O trabalho demonstra curadoria de fontes, engenharia de prompts, *grounding*, pensamento crítico, documentação e estudo introdutório de Open Finance.
