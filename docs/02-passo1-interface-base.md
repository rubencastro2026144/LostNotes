# Passo 1 — Interface base

Objetivo: ter a estrutura do site montada (páginas, cores, letras, menu e página inicial).
Ainda **sem imagens nem textos finais**, isso vem depois.

Tempo estimado: 45–60 min.

---

## 1.1 Confirmar o tema e as definições

1. **Aparência → Temas**: o **Twenty Twenty-Five** tem de estar ativo.
2. **Definições → Geral**: Título `LostNotes`, Descrição `Loja de discos de vinil`, Idioma Português, Fuso horário Lisboa.
3. **Definições → Ligações permanentes**: escolher **Nome do artigo** e guardar.

## 1.2 Criar as páginas (vazias por agora)

Em **Páginas → Adicionar**, criar e **publicar**:

| Título | Endereço (slug) esperado |
|---|---|
| Início | `/inicio/` |
| Sobre | `/sobre/` |
| Envios e Devoluções | `/envios-e-devolucoes/` |
| Contactos | `/contactos/` |
| Novidades | `/novidades/` |

> A página **Loja** já foi criada pelo WooCommerce. Confirma em **Páginas** qual é o endereço dela (deve ser `/loja/`). Se for diferente, avisa, porque os botões da página inicial apontam para `/loja/`.

Apagar a "Página de exemplo" e o artigo "Olá, mundo!".

## 1.3 Definir a página inicial

**Definições → Leitura**:
- "A sua página inicial mostra" → **Uma página estática**
- Página inicial: **Início**
- Página de artigos: **Novidades**

## 1.4 Cores (R04)

**Aparência → Editor → Estilos** (ícone de meia-lua) → **Cores** → **Paleta** → editar as cores do tema:

| Nome no editor | Cor nova |
|---|---|
| Base | `#141210` |
| Contraste | `#F2E8D5` |
| Destaque 1 (Accent 1) | `#E8572A` |
| Destaque 4 (Accent 4) | `#B8AE9C` |
| Destaque 5 (Accent 5) | `#221F1B` |

Depois, ainda em **Cores**:
- **Botão**: fundo **Destaque 1**, texto **Base**.
- **Ligação**: **Destaque 1**.

Gravar.

> Se o site ficar com alguma zona clara estranha, é porque essa secção usa outra cor da paleta. Diz-me qual e eu indico a cor certa.

## 1.5 Tipografia (R04)

**Estilos → Tipografia**:
- **Texto**: Manrope (já vem com o tema).
- **Títulos**: instalar uma letra forte. Em **Tipografia → Gerir fontes (ícone) → Instalar fontes**, permitir o acesso ao Google Fonts, procurar **Bebas Neue**, instalar e escolher em **Títulos**.
  - Se a opção de instalar fontes não aparecer, usar Manrope com peso **800** nos títulos.

Gravar.

## 1.6 Cabeçalho e menu (R03)

**Aparência → Editor → Padrões → Partes de template → Header** (cabeçalho):
1. Clicar no bloco **Navegação** → no painel da direita, editar o menu.
2. Deixar só estas ligações, por esta ordem: **Início · Loja · Sobre · Novidades · Contactos**.
3. Inserir à direita o bloco **Mini-carrinho** do WooCommerce.
4. Gravar.

## 1.7 Rodapé

**Partes de template → Footer**: apagar o que não interessa e deixar:
- Coluna 1: **LostNotes**, com a frase "Loja de discos de vinil" por baixo.
- Coluna 2: ligações **Envios e Devoluções** e **Contactos**.
- Coluna 3: morada e horário fictícios (ex.: Rua dos Discos 12, Porto · Seg–Sáb 11h–19h).
- Linha final: `© 2026 LostNotes — projeto académico`.

## 1.8 Página inicial

1. Abrir a página **Início** para editar.
2. Menu **⋮** (canto superior direito) → **Editor de código**.
3. Colar o conteúdo do ficheiro [`blocos/inicio.html`](../blocos/inicio.html).
4. Voltar ao **Editor visual** (mesmo menu).
5. Na secção "Acabados de chegar", apagar o parágrafo `[SUBSTITUIR…]` e inserir o bloco **Coleção de produtos** (WooCommerce) com 4 produtos. Se ainda não houver produtos, deixar para o passo da loja.
6. **Atualizar**.

## 1.9 CSS adicional (início do R07)

**Estilos → ⋮ → CSS adicional** → colar o conteúdo de [`css/lostnotes.css`](../css/lostnotes.css) → Gravar.

O botão "Ver discos" já tem a classe `ln-botao` vinda do passo 1.8.

## 1.10 Verificar

- [ ] O site abre na página **Início**.
- [ ] Todas as ligações do menu abrem a página certa.
- [ ] O botão "Ver discos" vai para a Loja.
- [ ] Ao passar o rato no "Ver discos", o botão sobe.
- [ ] Reduzir a janela até largura de telemóvel: o menu passa a ícone e os botões ocupam a largura toda.
- [ ] Carregar em **Tab** várias vezes: aparece um contorno laranja nas ligações.

Tirem **capturas de ecrã** já agora (computador e telemóvel). Vão fazer falta na nota técnica.

---

### O que é cada coisa

- **Código de blocos (`inicio.html`)**: é o mesmo formato que o editor do WordPress guarda. Os comentários `<!-- wp:... -->` dizem ao editor qual é o bloco e as opções dele. Depois de colado, editam tudo normalmente no editor visual.
- **CSS**: está explicado nos comentários do próprio ficheiro.
