# 🖨️ Custos Fixos — Precificação Impressão 3D

> **Como usar:** edite apenas os **valores** deste arquivo sempre que seus custos mudarem.
> Não altere os **nomes dos campos** nem a estrutura das tabelas — é por eles que o agente encontra cada variável.
> Valores monetários no formato brasileiro (vírgula como separador decimal). Ex.: `69,45`.

---

## 1. Filamentos — custo por cor

Cada cor tem seu próprio rolo e preço. O **custo por grama** é calculado automaticamente pelo agente: `custo do rolo ÷ peso do rolo`.

| Filamento                                      | Custo do rolo (R$) | Peso do rolo (g) |
|------------------------------------------------|-------------------:|-----------------:|
| PLA Branco Velvet High Speed Premium           | 91,07              | 1000             |
| PLA Verde Oliva Velvet High Speed Premium      | 85,36              | 1000             |
| PLA Marrom Cappuccino Velvet High Speed Premium| 85,36              | 1000             |
| PLA Vermelho Velvet High Speed Premium         | 85,36              | 1000             |
| PLA Marrom Velvet High Speed Premium           | 93,38              | 1000             |
| PLA Branco Pérola V-Silk High Speed Premium     | 93,38              | 1000             |
| PLA Azul Macaron Velvet High Speed Premium      | 104,99             | 1000             |
| PLA Rosa Bebê Velvet High Speed Premium         | 94,38              | 1000             |
| PLA Preto Velvet High Speed Premium             | 93,56              | 1000             |

**Filamento sem estoque:** PLA Verde High Speed Premium. Não utilizar em orçamentos até a reposição e atualização do preço.

> Os pesos foram mantidos em **1000 g por rolo**, conforme o padrão da tabela anterior. Para **adicionar uma cor**, copie uma linha e edite. Para **remover**, apague a linha.

---

## 2. Energia

| Variável                            | Valor |
|-------------------------------------|------:|
| Potência média da impressora (W)    | 60    |
| Custo do kWh (R$)                   | 0,96  |

> O custo de energia é: `(potência ÷ 1000) × tempo total em horas × custo do kWh`.

---

## 3. Embalagem, perdas e adicionais

| Variável                          | Valor   |
|-----------------------------------|--------:|
| Custo de embalagem (R$)           | 0,50    |
| Perdas (% sobre o custo de PLA)   | 5       |
| Argola de chaveiro (R$/unidade)   | 0,2054  |

> **Perdas** = 5% do custo de filamento gasto na peça (refugo, desperdício). Calculado: `0,05 × custo de filamento`.
> **Argola de chaveiro**: somada aos custos adicionais **apenas quando a peça for um chaveiro** — R$ 0,2054 por unidade.

---

## 4. Envio

| Variável                        | Valor |
|---------------------------------|------:|
| Custo de envio padrão (R$)      | 0,00  |

> Use `0,00` se você não arca com o frete (ex.: comprador paga ou Shopee subsidia).
> No pedido de orçamento você pode **informar um custo de envio específico**, que sobrepõe este padrão.

---

## 5. Taxas Shopee

Aplicadas **somente quando o envio for pela Shopee**.

| Variável                       | Valor |
|--------------------------------|------:|
| Comissão (%)                   | 14    |
| Taxa frete grátis (%)          | 6     |
| Taxa fixa por pedido (R$)      | 4,00  |
| Adicional CPF (R$)             | 0,00  |

> Comissão e frete grátis são percentuais **sobre o preço de venda**.
> Taxa fixa e CPF são valores fixos por pedido.

---

## 6. Meta de lucro

| Variável                       | Valor |
|--------------------------------|------:|
| Margem mínima desejada (%)     | 50    |
| Base da margem                 | preço de venda |

> **Base "preço de venda"** (padrão): margem = `lucro ÷ preço`. Uma margem de 50% significa que metade do preço final é lucro líquido.
> Se preferir calcular sobre o **custo** (markup), troque o campo "Base da margem" para `custo`. Aí margem de 50% = preço é o custo × 1,5.
> O agente sempre mostra **margem E markup** no resultado, independente da base escolhida.

---

### ✏️ Resumo do que editar com mais frequência
- **Preço dos rolos** (sobe e desce conforme o fornecedor) → seção 1
- **Custo do kWh** (muda na conta de luz) → seção 2
- **Taxas Shopee** (se a Shopee alterar a comissão) → seção 5
- **Margem alvo** (se quiser trabalhar com mais ou menos lucro) → seção 6
