# Projeto-final-html-e-css
# UniGestão - Sistema Acadêmico

Projeto final de **HTML e CSS** que simula um sistema acadêmico para o aluno consultar disciplinas, horários e provas em um só lugar.

O site é feito **somente com HTML e CSS**, sem JavaScript, e tem um **menu lateral fixo** para navegar entre as páginas.

## Páginas

| Página | Arquivo | O que tem |
|---|---|---|
| Início | `html/index.html` | Texto de boas-vindas e três cards com atalhos para Disciplinas, Horários e Provas |
| Disciplinas | `html/disciplinas.html` | Um card por matéria (professor, carga horária e sala), com ementa e bibliografia em `<details>` e âncoras no topo para pular para cada matéria |
| Horários | `html/horarios.html` | Tabela semanal (dias nas colunas, horários nas linhas) e legenda de cores por disciplina |
| Provas | `html/provas.html` | Tabela com data, disciplina, tipo (prova, trabalho, seminário) e conteúdo, mais uma lista numerada de dicas de estudo |
| Links úteis | `html/links.html` | Links separados por categoria: acesso do aluno e biblioteca/pesquisa |
| Contato | `html/contato.html` | Formulário com nome, e-mail, assunto (`<select>`) e mensagem (`<textarea>`). É só visual e não envia nada |

Todas as páginas têm o mesmo esqueleto: menu lateral, cabeçalho com o nome do site, conteúdo e rodapé.

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
│   └── contatos.css
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

## Como usar

1. Baixe ou clone o projeto.
2. Abra o arquivo `html/index.html` no navegador (dois cliques ou "Abrir com...").
3. Navegue pelo menu lateral.

Não é preciso instalar nada nem usar servidor.

## Regras seguidas no código

- **Um CSS por página HTML:** cada página carrega apenas o seu arquivo `.css`.
- **Estilização por `id`:** o CSS usa seletores com cerquilha (`#menu-lateral`, `#card-adm`, `#tabela-provas`), e cada `id` aparece uma única vez por página.
- **Exceção:** a legenda de cores dos horários usa **classes** (`.adm`, `.cont`, `.mat`, `.pes`, `.met`), porque a mesma cor se repete em várias células e um `id` não pode se repetir.
- **Tags simples:** `nav`, `header`, `main`, `section`, `footer`, `table`, `ul`, `ol`, `details`, `form`, entre outras básicas.

## Recursos usados

- Menu lateral fixo com `position: fixed`.
- Cards lado a lado com `display: flex`.
- `<details>` e `<summary>` para abrir e fechar conteúdo sem JavaScript.
- Âncoras internas (`href="#card-adm"`) para pular até cada disciplina.
- Tabelas com `border-collapse`.
- Ajuste simples para telas pequenas com `@media (max-width: 800px)`.

## Paleta de cores

Tiradas do logotipo:

| Cor | Código |
|---|---|
| Azul escuro | `#0b1f4b` |
| Dourado | `#e09400` |
| Fundo da página | `#f3f5fa` |

## Observações

- Os dados (professores, salas, horários e datas das provas) são **exemplos fictícios**. Troque pelos dados reais.
- Os links de portal do aluno, e-mail institucional e biblioteca estão com `#` e precisam receber os endereços reais. Só o link das normas ABNT aponta para um site de verdade.
- O formulário de contato é **apenas visual**: o botão não envia mensagem.
- O menu e o CSS base se repetem em todas as páginas, porque o projeto não usa JavaScript nem servidor. Para mudar uma cor ou um item do menu, é preciso alterar todos os arquivos.

## Tecnologias

- HTML5
- CSS3
