# LostNotes — Planeamento do projeto (R01)

> Rascunho. Vai sendo atualizado ao longo do projeto e serve de base à nota técnica.

## Identificação

| Campo | Valor |
|---|---|
| Nome | **LostNotes** |
| Percurso | **B — Loja com WooCommerce** |
| Tipo | Loja online fictícia de discos de vinil (novos e usados) |
| Objetivo | Permitir ao visitante descobrir e comprar discos de vinil |
| Público-alvo | Colecionadores e curiosos do vinil, 18–45 anos, que gostam de lojas de discos independentes |
| Ação principal | **Comprar um disco** (Loja → Produto → Carrinho → Finalizar compra) |
| Ambiente | LocalWP, WordPress, tema **Twenty Twenty-Five**, editor nativo |

## Mapa do site

| Conteúdo | Tipo | Função | Requisito |
|---|---|---|---|
| Início | Página | Apresentar a loja, mostrar destaques e levar à compra | R02 |
| Loja | Página WooCommerce | Catálogo de vinis | L01, L02 |
| Sobre | Página | História e valores da LostNotes | R02 |
| Envios e Devoluções | Página | Prazos, custos e política de devolução | R02 |
| Contactos | Página | Formulário de contacto, morada e horário | R02, R10 |
| Novidades | Página de artigos | Listagem dos artigos | R02 |
| Carrinho / Finalizar compra / Minha conta | Páginas técnicas WooCommerce | Processo de compra (não contam para as 4 páginas) | L02 |

### Artigos e categorias

| Categoria | Artigo inicial |
|---|---|
| Guias | Como cuidar dos teus discos de vinil |
| Lançamentos | Novos discos que chegaram à LostNotes este mês |

### Menu principal

Início · Loja · Sobre · Novidades · Contactos (+ ícone do carrinho)

### Rodapé

Envios e Devoluções · Contactos · morada e horário fictícios · © LostNotes

## Como a estrutura responde ao objetivo

- O **Início** apresenta a loja em poucos segundos e tem o botão "Ver discos" logo no topo.
- A **Loja** está sempre no menu, por isso a ação principal fica a um clique de qualquer página.
- **Envios e Devoluções** responde às dúvidas que costumam travar uma compra.
- Os **artigos** (guias e lançamentos) dão razões para voltar e levam aos produtos.

## Personalizações previstas

| Requisito | Proposta |
|---|---|
| R04 Estilos | Paleta escura (preto, creme, laranja), título com letra forte, texto em Manrope |
| R05 Template | **Página Informativa** — aplicado a *Sobre* e *Envios e Devoluções* |
| R06 Padrão | **Convite à Loja** (botão "Ver discos") — usado no Início e no Sobre |
| R07 CSS | Botões com efeito ao passar o rato, foco visível e ajuste em ecrã pequeno |

## Identidade visual

| Função | Cor | Uso |
|---|---|---|
| Base (fundo) | `#141210` | Fundo do site |
| Contraste (texto) | `#F2E8D5` | Texto e títulos |
| Destaque | `#E8572A` | Botões, ligações, detalhes |
| Superfície | `#221F1B` | Caixas e secções alternadas |
| Texto secundário | `#B8AE9C` | Legendas, datas |

Contraste calculado (WCAG): creme sobre preto ≈ **15:1**, laranja sobre preto ≈ **5,2:1**. Ambos passam o nível AA.
