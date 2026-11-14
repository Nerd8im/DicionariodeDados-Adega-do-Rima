# Dicionário de Dados - Adega do Rima

Dicionário de dados interativo do banco de dados do **Sistema de Gestão Operacional e Vendas** da Adega do Rima, desenvolvido na disciplina de Banco de Dados do curso de Análise e Desenvolvimento de Sistemas da UNICID (Tatuapé).

**Acesse o site:** https://nerd8im.github.io/DicionariodeDados-Adega-do-Rima/

## Sobre o projeto

A Adega do Rima é um varejo de bebidas com loja física única que controlava estoque e vendas de forma manual. O banco de dados proposto centraliza clientes, catálogo, pedidos, pagamentos, estoque por lote com controle de validade, cancelamento e estorno, auditoria e atendimento aos direitos do titular da LGPD.

Este repositório publica o dicionário de dados desse banco, organizado com base em boas práticas de governança de dados (DAMA-DMBOK e COBIT).

## O que o site oferece

- 20 tabelas e 130 colunas, com atributo, descrição e regra de negócio, tipo e tamanho, constraints, privacidade, linhagem e controle de acesso.
- Classificação de privacidade por coluna, conforme a LGPD: `[DPS]` dado pessoal sensível, `[DP]` dado pessoal e `[N/A]` não aplicável.
- Controle de acesso por perfil (Atendente, Gerente e Administrador).
- Busca em tempo real por nome de tabela ou de coluna.
- Menu lateral com âncoras para todas as tabelas, adaptado a celulares.
- Visualizador do DER em tela cheia, com zoom pelo scroll, arraste da imagem e botões de zoom e reset.
- Alternância entre modo claro e modo escuro.
- Download da Especificação de Requisitos e Regras de Negócio em PDF.

## Estrutura do repositório

```text
.
├── index.html
├── style.css
├── script.js
├── docs/
│   └── Especificacao_Requisitos_Regras_Negocio_BD.pdf
└── assets/
    └── der.png
```

| Arquivo | Função |
|---|---|
| `index.html` | Estrutura da página, identificação do projeto e modal do DER |
| `style.css` | Identidade visual, temas claro e escuro e layout responsivo |
| `script.js` | Dados das tabelas e colunas, busca, tema, menu e visualizador do DER |
| `docs/` | Especificação de Requisitos e Regras de Negócio em PDF |
| `assets/` | Imagem do Diagrama Entidade-Relacionamento |

## Tecnologias

- HTML5, CSS3 e JavaScript, sem etapa de build.
- [Panzoom](https://github.com/timmywil/panzoom) 4.5.1, carregado pelo jsDelivr, para zoom e navegação no DER.
- Banco de dados documentado: MySQL 8.4 LTS, engine InnoDB, charset utf8mb4.

## Como executar localmente

1. Clone o repositório:

   ```bash
   git clone https://github.com/Nerd8im/DicionariodeDados-Adega-do-Rima.git
   cd DicionariodeDados-Adega-do-Rima
   ```

2. Abra o `index.html` no navegador. Se o PDF ou o DER não carregarem, sirva a pasta por um servidor local:

   ```bash
   python -m http.server 8000
   ```

   Depois acesse `http://localhost:8000`.

## Publicação

O site é publicado pelo GitHub Pages, a partir da branch `main` na pasta raiz (`Settings > Pages > Build and deployment > Source: Deploy from a branch`).

O GitHub Pages diferencia maiúsculas de minúsculas nos caminhos. Mantenha os nomes `docs/`, `assets/` e `der.png` exatamente como estão.

## Equipe

Grupo 3

- Gabriel Anjos Albuquerque (líder do grupo e Data Owner)
- Rafael Christian de Araujo Costa (analista de requisitos e Data Steward)
- Luan Henrique Ribeiro de Albuquerque
- Thiago Nielsen dos Santos
- Arthur Costa de Paula
- Mateus Izac Batista
- Ana Julia de Aquino Silva

**Professor orientador:** Prof. Diego Marques de Carvalho

**Instituição:** Universidade Cidade de São Paulo (UNICID), Tatuapé, Análise e Desenvolvimento de Sistemas, disciplina de Banco de Dados.

## Observação

Projeto acadêmico. As regras de negócio, as políticas legais e as premissas de carga e desempenho estão descritas na Especificação de Requisitos e Regras de Negócio disponível em `docs/`.
