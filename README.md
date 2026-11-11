# UniGestão - Sistema Acadêmico

Projeto final de **HTML e CSS** que simula um portal acadêmico onde o aluno consulta, em um só lugar, as disciplinas do semestre, o quadro de horários e o calendário de provas.

O site usa **apenas HTML5 e CSS3** (sem JavaScript, sem frameworks e sem servidor) e conta com um **menu lateral fixo** para navegar entre as páginas.

## Visão geral

| Item | Detalhe |
|---|---|
| Tema | Sistema acadêmico para o aluno de graduação (curso de Administração) |
| Páginas | 6 |
| Tecnologias | HTML5 e CSS3 |
| Dependências | Nenhuma |
| Idioma | Português (pt-BR) |

## Páginas

| Página | Arquivo | Conteúdo |
|---|---|---|
| Início | `html/index.html` | Boas-vindas e três cards de atalho para Disciplinas, Horários e Provas |
| Disciplinas | `html/disciplinas.html` | Um card por matéria com professor, carga horária e sala. Ementa e bibliografia ficam em `<details>`, e há âncoras no topo para ir direto a cada disciplina |
| Horários | `html/horarios.html` | Tabela semanal (dias nas colunas, horários nas linhas) e legenda de cores por disciplina |
| Provas | `html/provas.html` | Tabela com data, disciplina, tipo (prova, trabalho ou seminário) e conteúdo, além de uma lista numerada de dicas de estudo |
| Links úteis | `html/links.html` | Links organizados em "Acesso do aluno" e "Biblioteca e pesquisa" |
| Contato | `html/contato.html` | Formulário com nome, e-mail, assunto (`<select>`) e mensagem (`<textarea>`) |

Todas as páginas seguem o mesmo esqueleto: **menu lateral**, **cabeçalho** com o nome do sistema, **conteúdo principal** e **rodapé**.

### Disciplinas cadastradas (dados de exemplo)

- Administração Geral
- Contabilidade Básica
- Matemática Financeira
- Gestão de Pessoas
- Metodologia Científica

## Estrutura de pastas

```
Projeto-final-html-e-css/
├── README.md
├── css/
│   ├── index.css
│   ├── disciplinas.css
│   ├── horarios.css
│   ├── provas.css
│   ├── links.css
│   └── contatos.css      (usado por contato.html)
├── html/
│   ├── index.html
│   ├── disciplinas.html
│   ├── horarios.html
│   ├── provas.html
│   ├── links.html
│   └── contato.html
└── img/
    └── logotipo.png
```

## Como executar

1. Baixe o projeto (botão **Code > Download ZIP**) ou clone o repositório:
   ```bash
   git clone https://github.com/kleytonmichel15-droid/Projeto-final-html-e-css.git
   ```
2. Abra o arquivo `html/index.html` no navegador (dois cliques ou "Abrir com...").
3. Navegue pelo menu lateral.

Não é preciso instalar nada.

## Boas práticas e regras seguidas

- **Um CSS por página:** cada HTML carrega somente o seu próprio arquivo `.css`.
- **Estilização por `id`:** os seletores usam cerquilha (`#menu-lateral`, `#card-adm`, `#tabela-provas`), e cada `id` aparece uma única vez por página.
- **Exceção planejada:** a legenda de cores dos horários usa **classes** (`.adm`, `.cont`, `.mat`, `.pes`, `.met`), pois a mesma cor se repete em várias células e um `id` não pode se repetir.
- **Tags semânticas básicas:** `nav`, `header`, `main`, `section`, `footer`, `table`, `ul`, `ol`, `details`, `form`.
- **Acessibilidade básica:** `lang="pt-BR"`, texto alternativo no logotipo e `<label>` associado a cada campo do formulário.

## Recursos de HTML e CSS utilizados

- Menu lateral fixo com `position: fixed`.
- Cards lado a lado com `display: flex` e `flex-wrap`.
- `<details>` e `<summary>` para abrir e fechar conteúdo sem JavaScript.
- Âncoras internas (`href="#card-adm"`) para saltar até cada disciplina.
- Tabelas com `border-collapse`.
- Efeitos de `:hover` no menu e nos botões.
- Responsividade simples com `@media (max-width: 800px)`: o menu deixa de ser fixo e passa a ocupar o topo da página.
- Meta tag `viewport` para boa exibição em celulares.

## Paleta de cores

Cores extraídas do logotipo:

| Cor | Código | Uso |
|---|---|---|
| Azul escuro | `#0b1f4b` | Menu lateral, títulos e rodapé |
| Dourado | `#e09400` | Detalhes, bordas e destaque ao passar o mouse |
| Fundo da página | `#f3f5fa` | Plano de fundo |

## Observações

- Professores, salas, horários e datas das provas são **dados fictícios**; substitua pelos dados reais.
- Os links do portal do aluno, do e-mail institucional e da biblioteca virtual estão como `#` e precisam receber os endereços reais. Apenas o link das normas ABNT aponta para um site de verdade.
- O formulário de contato é **apenas visual**: o botão "Enviar" não envia mensagem (isso exigiria JavaScript ou um servidor).
- O menu e o CSS base se repetem em todas as páginas, já que o projeto não usa JavaScript nem servidor. Para mudar uma cor ou um item do menu, é preciso editar todos os arquivos.

## Ideias de melhorias futuras

- Tornar o formulário funcional (JavaScript ou serviço de formulários).
- Unificar o CSS repetido em um arquivo base compartilhado.
- Adicionar mais disciplinas, períodos e uma página de notas e frequência.
- Publicar o site no GitHub Pages.

## Tecnologias

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
