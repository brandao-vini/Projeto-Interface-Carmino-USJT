# Projeto Interfaces - José Carmino


![alt text](/assets/img/image.png)

# Sobre o Projeto

Este projeto consiste na reconstrução fiel de interfaces web a partir de wireframes estáticos, com foco em demonstrar proficiência em HTML5 semântico e CSS moderno. A implementação segue rigorosamente a metodologia mobile-first, utilizando Flexbox e Grid para garantir um layout responsivo e acessível em dispositivos de 320px a 1440px. Além disso, o desenvolvimento prioriza as boas práticas de acessibilidade (WCAG AA), como o uso de variáveis CSS para escalas tipográficas consistentes e a garantia de contraste adequado para uma melhor experiência do usuário.



## 🖥️ Telas Implementadas

| Arquivo | Tela | Descrição |
| :--- | :--- | :--- |
| `index.html` | Home | Navegue por tópicos de interesse  |
| `listagem.html` | Categoria: Techno | Listagem de posts por categoria  |
| `destaques.html` | Destaques | Visualização dos posts em destaque |
| `assinar.html` | Assinar | Inscrição na newsletter |
| `busca.html` | Resultados | Resultados da pesquisa no site |
| `entrar.html` | Login | Acesso à conta do usuário |
| `cadastro.html` | Criar Conta | Cadastro de novos usuários no sistema |
| `perfil.html` | Perfil | Visualização de dados e postagens do usuário logado |
| `admin-categorias.html` | Admin: Categorias | Gerenciamento de tópicos |
| `admin-criar-post.html` | Admin: Criar Post | Interface de criação de conteúdo |
| `admin-escolhas.html` | Admin: Escolhas | Gestão das escolhas do editor |
| `admin-usuarios.html` | Admin: Usuários | Controle de usuários do sistema |
| `admin-revisao.html` | Admin: Revisão | Fila de aprovação de postagens |
| `admin-comentarios.html` | Admin: Comentários | Moderação de comentários |

---


# Decisões de Layout

- CSS Grid para o grid de postagens (1 → 2 → 3 colunas conforme a tela cresce) e para o layout admin (sidebar + conteúdo).

- Flexbox para header, nav, grupos de botões, stats bar e footer de links.

- Sem frameworks – apenas CSS puro com variáveis em `:root`.

- Placeholders de imagem implementados com `background: var(--color-card-bg)` e `role="img" + aria-label`, conforme orientação do exercício.

- Escala tipográfica rigorosa: h1 = 2.5rem, h2 = 2rem, h3 = 1.5rem, body = 1rem, small = 0.875rem.

- Tokens de espaçamento (`--space-xs` a `--space-2xl`) usados de forma consistente em todas as páginas.

- Paleta de cores baseada no mockup: teal (`#1a7a6e`) para botões primários, coral (`#e76f51`) para Admin e ações de perigo, cinza claro para bordas.

# Breakpoints Utilizados

A abordagem adotada foi o **Mobile-First**, onde o CSS base é escrito focado em telas pequenas e as `media queries` com `min-width` adicionam complexidade e novos elementos ao layout progressivamente.

#### Tabela de Breakpoints

| Breakpoint | Valor | Ajuste Principal |
| :--- | :--- | :--- |
| **Base (Padrão)** | ≤ 480px | Layout em 1 coluna, títulos reduzidos e footer em coluna única. |
| **Celular Médio** | 481px | O grid de posts passa a exibir 2 colunas. |
| **Tablet** | 768px | Layout administrativo ativo (sidebar + conteúdo) e ampliação da barra de busca. |
| **Desktop** | 1024px | Grid de posts com 3 colunas e aumento do padding no `wrapper`. |
| **Monitor Grande** | 1440px | Valor de `--container-max` expandido para 960px para melhor aproveitamento de tela. |


# ♿ Acessibilidade e Boas Práticas (WCAG 2.1 AA)

A implementação seguiu rigorosamente os padrões de acessibilidade e semântica exigidos para garantir uma experiência inclusiva e um código de alta qualidade:

* **Semântica HTML5:** Uso correto das tags estruturais `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>` e `<footer>` em todas as páginas para definir a arquitetura da informação.
* **Hierarquia de Títulos:** Cada página possui um único `<h1>` como título principal, com subtítulos seguindo a sequência lógica h2 → h3 para manter a estrutura hierárquica.
* **Acessibilidade em Formulários:** Todos os elementos `<input>` possuem uma `<label>` vinculada via `for/id`. Campos obrigatórios utilizam os atributos `required` e `aria-required="true"`.
* **Imagens e Placeholders:** Uso de `max-width: 100%` e `height: auto` para garantir imagens fluidas.
    * Placeholders de imagem utilizam `role="img"` e `aria-label` descritivo para leitura por tecnologias assistivas.
* **Navegação e Foco:**
    * Aplicação de `aria-current="page"` no link da página atual para orientação do usuário.
    * Foco visível garantido via `:focus-visible` com `outline` de 3px em todos os elementos interativos.
    * Navegação por teclado completa, sem o uso de `tabindex` negativo em elementos essenciais.
* **Estratégia `.sr-only`:** Utilização da classe para labels que precisam ser invisíveis visualmente (como na busca do header), mas legíveis por leitores de tela.
* **Contraste de Cores (WCAG AA):**
    * **Texto Principal:** Texto escuro (`#1e2022`) sobre fundo branco (razão 18.1:1).
    * **Texto Secundário:** Texto cinza (`#6c757d`) sobre branco (razão 4.54:1), atendendo ao mínimo de 4.5:1.
    * **Componentes:** Botões primários com branco sobre teal (`#1a7a6e`) mantendo a relação de 4.6:1.
* **Estados Interativos:** Definição completa de estilos para os estados `:hover`, `:focus`, `:active` e `:disabled`.






# Índice/Sumário

* [Sobre](#sobre-o-projeto)
* [Sumário](#índice/sumário)
* [Tecnologias Usadas](#tecnologias-usadas)
* [Contribuição](#contribuição)
* [Autores](#autores)
* [Licença](#licença)
* [Agradecimentos](#agradecimentos)




# Tecnologias Usadas

- [HTML5](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
- [CSS3](https://developer.mozilla.org/pt-BR/docs/Web/CSS)

# Contribuição

Leia o arquivo [CONTRIBUTING.md](CONTRIBUTING.md) para saber detalhes sobre o nosso código de conduta e o processo de envio de solicitações *pull* (*Pull Request*) para nós.

# Autores

- [Anna Clara](https://github.com/annasilvas)
- [Stela Camargo](https://github.com/StelaCamargo)
- [Pedro Miranda](https://github.com/PedroMR364)
- [Vinícius Brandão](https://github.com/brandao-vini)

# Licença

Este projeto está licenciado sob a Licença MIT,  consulte o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

# Agradecimentos

Gostaria de expressar meu agradecimento aos integrantes do grupo pela colaboração e dedicação no desenvolvimento deste projeto:


- Anna Clara: Pela importante contribuição na estruturação e organização do trabalho.  


- Pedro Miranda: Pelo empenho no versionamento e compromisso com os prazos estabelecidos.  


- Stela Camargo: Pela dedicação na implementação técnica e auxílio na qualidade do código.  

Este esforço conjunto foi fundamental para garantirmos que todos os requisitos de semântica, responsividade e acessibilidade fossem atendidos conforme as diretrizes da disciplina.
