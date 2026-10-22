# Explorador Anatômico

**Acesse:** https://pedrongjr.github.io/explorador-anatomico/

Página web (HTML5 + WebGL) para explorar um corpo humano em 3D, no estilo do Google Earth: girar, aproximar, voar até uma região e clicar em qualquer estrutura para ver nome em português, nome latino e descrição.

## Como abrir

A página carrega os modelos da pasta `modelos/` por `fetch`, então precisa ser servida por HTTP (abrir o arquivo direto com duplo clique não funciona na maioria dos navegadores):

```

python3 -m http.server 8000
# abra http://localhost:8000
```

O site é publicado pelo GitHub Pages a partir da branch `main` (pasta raiz); cada push atualiza a página em cerca de um minuto. O primeiro acesso baixa cerca de 20 MB; músculos, articulações, fáscias e linfático (mais ~12 MB) só são baixados quando a camada é ligada.

## O que tem

- **Modelos anatômicos reais do Z-Anatomy**: cerca de 3.100 peças em 16 camadas (pele e unhas, músculos, fáscias, esqueleto, articulações e ligamentos, coração, artérias, veias, respiratório, digestório, urinário, endócrino, nervoso, olhos e orelhas, linfático, pleura e peritônio). Inclui giros do cérebro, segmentos do fígado, árvore brônquica segmentar, valvas do coração, nervos periféricos com ramos digitais e 760 pontos de referência (acidentes ósseos, partes do rosto) que aparecem ao aproximar.
- **Corpo neutro**: o sistema genital, os pelos pubianos e o cabelo foram removidos dos modelos.
- **Tudo em português do Brasil**: nomes revisados e padronizados (com o termo em latim abaixo) e descrições em português para as quase 1.300 estruturas que tinham resumo no Z-Anatomy; as demais têm uma descrição geral do grupo em português.
- **Percursos animados** da comida (11 etapas) e da água (13 etapas), passando pelos órgãos e vasos reais, com peristaltismo, tempo real de cada fase, legenda e diagramas (vilosidade intestinal, néfron).
- **Legendas na tela** que aparecem conforme cada estrutura fica grande o bastante, busca, isolar/ocultar, cortes sagital, coronal e transversal, fluxo sanguíneo, batimento e respiração animados.
- **Diagramas** da pele, da unha, do néfron e da vilosidade.

`versao-procedural.html` é a versão anterior, com o corpo gerado inteiramente por código (mais leve, abre sem servidor, menos detalhada).

## Licença dos modelos

Os modelos em `modelos/` são derivados do Z-Anatomy e distribuídos sob CC BY-SA 4.0; veja `modelos/LICENCA.md`. É um material didático, não um substituto de atlas médico.
