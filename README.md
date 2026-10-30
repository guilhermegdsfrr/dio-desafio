[README.md](https://github.com/user-attachments/files/34187208/README.md)
# Painel de vendas Porsche

Dashboard em HTML (arquivo único) que responde perguntas de negócio sobre 100 vendas fictícias de Porsche no Brasil, de 2021 a 2025. Feita para o desafio do Curso Criando Agentes de Tratamento de Dados (DIO).

**Endereço da dashboard publicada:** `https://guilhermegdsfrr.github.io/Dio-Desafio/`

## Perguntas de negócio escolhidas, e por quê

1. **Quais modelos concentram a receita?** Mostra onde está o dinheiro. Um modelo pode vender pouco e pesar muito na receita por causa do preço, e o gráfico de barras deixa isso visível.
2. **As vendas estão crescendo?** A receita por ano mostra a tendência e o melhor ano. É a pergunta que qualquer gestor faz primeiro.
3. **Como os clientes pagam, e isso muda de região para região?** A forma de pagamento influencia o planejamento comercial, como crédito, parcerias com bancos e consórcios. Como a base varia por região, a pergunta mostra diferenças reais: o Nordeste paga mais por financiamento e o Sudeste mais à vista.

Escolhi três perguntas, e não oito gráficos, para que cada uma tenha uma resposta clara. Cada gráfico traz uma frase de conclusão que se atualiza conforme os filtros.

Além das perguntas, a tela tem indicadores de topo (total de vendas, receita e ticket médio) e filtros por modelo, estado, ano e forma de pagamento.

## O prompt que gerou a dashboard, e o que mudou nele

Versão final do pedido, resumida:

```
Crie uma dashboard em HTML, arquivo único, com 100 vendas de Porsche
(modelo, cidade, estado, ano, preço e método de pagamento).
Preciso de três perguntas de negócio, cada uma respondida por um
gráfico, indicadores de topo (vendas, receita, ticket médio) e filtros
por modelo, estado, ano e pagamento. Os dados podem ser inventados, mas
devem variar por região. Visual coerente, com paleta e tipografia
definidas, pronta para publicar no GitHub Pages.
```

O que mudou até a versão final:

- **Versão inicial:** o pedido era só o enunciado do desafio, sem a base de dados.
- **Mudança principal:** passei a pedir que os dados fossem inventados e que **variassem por região**. Isso definiu a terceira pergunta, que compara a forma de pagamento entre regiões, e fez o modelo mais vendido mudar de uma região para outra.

## Tratamento da base antes de ir para a IA

A base não veio de uma planilha real: ela foi **gerada por um script** com uma semente fixa, então o resultado é reproduzível. Por isso não houve o passo de limpar registros `INVALID` da base crua. Mesmo assim, apliquei os cuidados que o desafio pede:

- Preço e ano são **números**, não texto.
- Os dados são **valores**, sem fórmulas que possam quebrar.
- Só ficaram as colunas necessárias: modelo, cidade, estado, ano, preço e pagamento.
- Os modelos só aparecem nos anos em que fazem sentido (o Taycan, por exemplo, não aparece em 2021).
- Os dados são **100% fictícios**, sem nenhum dado sensível, já que a base vai embutida no HTML.

## Ferramenta usada

Usei **um assistente de IA em chat (Claude)**, com geração do HTML e ajustes em linguagem natural. Não usei o ChatGPT com Canvas nem um agente com skill própria.

## Como abrir

Abra o endereço da dashboard publicada acima. Para rodar localmente, abra o arquivo `index.html` no navegador.
