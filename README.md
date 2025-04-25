# Projeto: Site de Divulgação de Produtos com Links de Afiliado

## Objetivo
Criar um site para divulgar produtos com links de afiliado, onde eu possa editar os produtos e links sempre que quiser. O site terá um sistema de **login e senha** para que os usuários possam se cadastrar e receber ofertas por e-mail.

---

## Funcionalidades desejadas

- Cadastro e login de usuários.
- Edição de produtos com links de afiliado, imagens e preços.
- Sistema de envio de ofertas e promoções por e-mail.
- Visualização dos produtos cadastrados.
- Filtro por categorias, tags e preço.
- Gerenciamento dos produtos e links de afiliado.
- Painel de controle para editar, excluir ou adicionar novos produtos.

---

## Estrutura da Base de Dados

### # Tabela: Usuários
- **id** (UUID): Identificador único do usuário
- **nome** (Texto): Nome completo do usuário
- **email** (Texto): E-mail do usuário
- **senha** (Texto): Senha criptografada
- **data_cadastro** (Data/hora): Data de cadastro do usuário

---

### # Tabela: Produtos
- **id** (UUID): Identificador único do produto
- **titulo** (Texto): Nome do produto
- **descricao** (Texto): Descrição detalhada do produto
- **categoria** (Texto): Categoria do produto (ex: moda, tecnologia, casa)
- **imagem_url** (URL): Link da imagem do produto
- **preco** (Numérico): Preço do produto
- **link_afiliado** (URL): Link do produto com código de afiliado
- **ativo** (Booleano): Produto está ativo? (Sim/Não)
- **data_criacao** (Data/hora): Data de criação do produto
- **data_ultima_edicao** (Data/hora): Data da última edição

---

### # Tabela: Ofertas
- **id** (UUID): Identificador único da oferta
- **titulo** (Texto): Título da oferta
- **descricao** (Texto): Descrição da oferta
- **data_inicio** (Data/hora): Data de início da oferta
- **data_fim** (Data/hora): Data de fim da oferta
- **produto_id** (UUID): Relacionamento com a tabela Produtos
- **link_oferta** (URL): Link para a página da oferta

---

### # Tabela: Envio de Ofertas por E-mail
- **id** (UUID): Identificador único do envio
- **usuario_id** (UUID): Relacionamento com a tabela Usuários
- **oferta_id** (UUID): Relacionamento com a tabela Ofertas
- **data_envio** (Data/hora): Data do envio do e-mail

---

## Funcionalidades Técnicas

1. **Login e Cadastro de Usuários**
   - Sistema de login com e-mail e senha criptografada.
   - Recuperação de senha via e-mail.

2. **Painel de Controle**
   - Para adicionar, editar e excluir produtos.
   - Para gerenciar ofertas e links de afiliado.
   - Visibilidade das ofertas enviadas aos usuários.

3. **Envio de E-mails**
   - Enviar e-mails automaticamente para os usuários cadastrados com ofertas.
   - Personalizar as ofertas enviadas com base no histórico de navegação ou preferências.

---

## Sugestões de Implementação

- **Frontend:** Utilize HTML, CSS e JavaScript para a interface do usuário.
- **Backend:** Use uma plataforma como Node.js ou Python (Flask/Django) para gerenciar o login, o envio de e-mails e as atualizações dos produtos.
- **Banco de Dados:** Pode usar Supabase, Firebase ou MySQL para armazenar os dados.
- **Envio de E-mail:** Utilize uma ferramenta como **SendGrid**, **Mailgun** ou **Amazon SES** para enviar as ofertas.
# ANA-links
