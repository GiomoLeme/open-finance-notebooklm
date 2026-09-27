# Engenharia de prompts

Foram realizados três experimentos A/B. Em cada caso, o Prompt A é mais aberto e o Prompt B adiciona público, estrutura, critérios de evidência ou distinções conceituais. Os prompts abaixo foram preservados como registrados no caderno.

## Experimento 1 - Definição de Open Finance

### Prompt A - simples

```text
O que é Open Finance?
```

### Prompt B - melhorado

```text
Com base exclusivamente nas fontes deste notebook, explique o que é Open Finance para uma pessoa sem conhecimento prévio sobre o sistema financeiro. Organize a resposta em quatro partes: definição, problema que busca resolver, como funciona e um exemplo prático. Para cada parte, indique quais fontes sustentam as principais afirmações. Caso alguma informação não esteja disponível nas fontes, deixe isso explícito.
```

### Observação e conclusão

O prompt simples gerou uma resposta correta, porém genérica. Ao definir o público-alvo, a estrutura e a exigência de indicação das fontes, a resposta ficou mais didática e rastreável. O experimento mostrou que especificar formato e critérios aumenta a utilidade sem necessariamente mudar os conceitos centrais.

## Experimento 2 - APIs

### Prompt A - simples

```text
Como funcionam as APIs no Open Finance?
```

### Prompt B - melhorado

```text
Utilizando somente informações sustentadas pelas fontes deste notebook, explique como as APIs são utilizadas no Open Finance para um estudante iniciante de desenvolvimento backend. Primeiro apresente uma analogia simples e depois uma explicação técnica. Diferencie claramente informações confirmadas pelas fontes de qualquer interpretação. Não inclua protocolos, tecnologias, endpoints ou padrões técnicos que não estejam explicitamente presentes nas fontes consultadas. Indique as referências utilizadas.
```

### Observação e conclusão

O prompt inicial produziu uma explicação geral válida, mas uma resposta anterior do NotebookLM havia extrapolado o conteúdo das fontes ao apresentar detalhes específicos de implementação. Com a restrição explícita, o modelo reconheceu que OAuth 2.0, OpenID Connect, FAPI, mTLS, JWT, formatos de payload e endpoints não estavam documentados no conjunto consultado.

Este foi o principal caso de troubleshooting do projeto. Ele mostrou que precisão aparente não equivale a suporte documental e que perguntas técnicas exigem limites claros de evidência.

### Checklist de grounding aplicado ao caso

- A afirmação aparece explicitamente em alguma fonte?
- É possível indicar a fonte correspondente?
- O texto diferencia fatos, analogias e interpretações?
- Protocolos e detalhes de implementação foram confirmados?
- Quando não há evidência, a resposta declara a lacuna?

## Experimento 3 - Segurança e riscos

### Prompt A - simples

```text
Open Finance é seguro?
```

### Prompt B - melhorado

```text
Com base exclusivamente nas fontes deste notebook, analise a segurança do Open Finance. Separe a resposta em: mecanismos de segurança do próprio ecossistema, riscos diretamente relacionados ao Open Finance e riscos gerais da digitalização financeira que não são exclusivos do Open Finance. Para cada risco ou mecanismo, indique a fonte correspondente. Não transforme riscos gerais do sistema financeiro digital em riscos específicos do Open Finance.
```

### Observação e conclusão

O prompt simples tratou segurança de forma ampla. A versão melhorada exigiu a separação entre mecanismos internos, riscos ligados ao uso do ecossistema e riscos gerais da digitalização financeira. Essa estrutura reduziu generalizações e evitou atribuir ao Open Finance problemas pertencentes ao ambiente financeiro digital em sentido mais amplo.

## Síntese dos aprendizados

1. Definir o público melhora o nível de linguagem e a utilidade da resposta.
2. Solicitar estrutura facilita comparação e revisão.
3. Exigir fontes aumenta a rastreabilidade, mas ainda demanda conferência humana.
4. Instruir o modelo a declarar lacunas reduz o preenchimento indevido com conhecimento externo.
5. Separar categorias próximas evita conclusões excessivamente amplas.
