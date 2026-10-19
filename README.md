# Ramen Me — proposta de redesign

Proposta de novo site para o [Ramen Me](https://ramenme.pt/), bar de ramen na Rua da Picaria 20, Porto. Estética street e noturna, com néon vermelho, alinhada com o [Instagram](https://www.instagram.com/ramenme.pt/) e com a sala.

## O que tem

- **Páginas:** Início, Menu, Reservas (com Uber Eats e takeaway), W/ Beats, Contacto (com Recrutamento) e Privacidade, numa única página com navegação por `#hash` (`#menu`, `#reservas`, `#beats`, `#contacto`, `#uber`, `#recrutamento`, `#alergenios`, `#privacidade`).
- **PT / EN:** botão no topo; a escolha fica guardada no navegador.
- **Menu interativo:** categorias, filtros Vegan e Picante, pesquisa, ficha de cada prato e um "talão" que soma o total.
- **W/ Beats:** contagem decrescente até ao próximo DJ e arquivo das noites passadas.
- **Estado aberto/fechado** calculado pela hora de Lisboa.
- **Mobile:** menu de ecrã inteiro e layout adaptado.

## Estrutura

```
index.html          HTML, CSS e JS num só ficheiro, sem dependências de build
img/                fotografias (redimensionadas a 1100 px)
assets/logo.svg     logo vetorizado a partir de uma captura (wordmark + katakana)
assets/logo-wordmark.svg
assets/favicon.svg  mascote da placa da rua
```

## Correr localmente

Qualquer servidor estático serve:

```
python3 -m http.server 8000
```

e abrir `http://localhost:8000`. Também abre diretamente no navegador.

## Antes de pôr em produção

- **Formulários** (reserva, newsletter, candidatura) não enviam nada: validam e mostram um resumo. Falta ligá-los a um backend ou serviço de email.
- **Fotos dos pratos:** algumas foram atribuídas por aproximação; gyozas, ebi furai, tofu don e sobremesas não têm foto e mostram o kanji em néon.
- **Agenda W/ Beats e menu** estão como dados no próprio `index.html` (`NIGHTS`, `DISHES`, `DRINKS`).
- **Política de Privacidade** é um texto resumido provisório.
- O logo foi extraído de uma imagem de baixa resolução; se existir o ficheiro original, vale a pena substituí-lo.
