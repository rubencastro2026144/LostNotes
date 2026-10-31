# Passo 1 — O que foi aplicado no site

Aplicado a 31/10/2026 com o WP-CLI do Local. Tudo fica editável no painel do WordPress.

Backups feitos antes das alterações (pasta do site no Local, não estão no repositório):
`backups/antes-passo1-20261031-1206.sql` e `backups/antes-inicio-css-20261031-1235.sql`.

## Onde ver cada coisa

| O quê | Valor | Onde ver |
|---|---|---|
| Título e descrição | LostNotes / Loja de discos de vinil | Definições → Geral |
| Idioma e fuso | Português (Portugal) / Lisboa | Definições → Geral |
| Ligações permanentes | Nome do artigo | Definições → Ligações permanentes |
| Páginas | Início, Sobre, Envios e Devoluções, Contactos, Novidades | Páginas |
| Exemplos removidos | "Sample Page" e "Hello world!" (no lixo) | Páginas / Artigos → Lixo |
| Leitura | Página inicial = Início; artigos = Novidades | Definições → Leitura |
| Paleta | Base #141210, Contraste #F2E8D5, Accent 1 #E8572A, Accent 4 #B8AE9C, Accent 5 #221F1B | Aparência → Editor → Estilos → Cores → Paleta |
| Botões e ligações | Botões: fundo Accent 1, texto Base. Ligações: Accent 1 | Estilos → Cores |
| Tipos de letra | Texto Manrope; títulos Bebas Neue | Estilos → Tipografia |
| Menu "Menu principal" | Início · Loja · Sobre · Novidades · Contactos | Editor → Navegação |
| Cabeçalho | Título do site, menu, mini-carrinho | Editor → Padrões → Partes de template → Header |
| Rodapé | Nome e descrição, ligações, morada e horário fictícios, © | Editor → Padrões → Partes de template → Footer |
| Página inicial | Conteúdo de `blocos/inicio.html` | Páginas → Início |
| CSS adicional | Conteúdo de `css/lostnotes.css` | Estilos → ⋮ → CSS adicional |

## Decisões

- A Loja ficou em `/shop/`, o endereço criado pelo WooCommerce. O link de `blocos/inicio.html` foi corrigido de `/loja/` para `/shop/`.
- Foram instaladas as traduções em português do WordPress, do WooCommerce e do tema.

## Verificação (lista 1.10 do guia)

Testado no site sem sessão iniciada, com o modo "Em breve" desligado durante o teste:

- [x] O site abre na página Início.
- [x] As ligações do menu apontam para a página certa e as páginas respondem.
- [x] O botão "Ver discos" aponta para a Loja.
- [x] Ao passar o rato, o botão sobe 3px e escurece.
- [x] A 375px o menu passa a ícone e o "Ver discos" ocupa a largura toda. O botão em contorno não, porque o CSS só se aplica a `.ln-botao`.
- [x] Com Tab aparece o contorno laranja.

## Por fazer

- Confirmar no editor que o Header, o Footer e a página Início abrem sem avisos de bloco inválido.
- Retirar o título "Início" que aparece por cima da secção de abertura (vem do template Páginas).
- Substituir o parágrafo `[SUBSTITUIR…]` pelo bloco Coleção de produtos, no passo da loja.
- Desligar o modo "Em breve" do WooCommerce antes da apresentação.
- Tirar as capturas de ecrã para a nota técnica.
- R05 (template) e R06 (padrão), à mão no editor.
