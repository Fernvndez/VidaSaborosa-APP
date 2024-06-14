# Vida Saborosa - Aplicativo de Entrega de Comida

## Sobre o Projeto

O *Vida Saborosa* é um aplicativo desenvolvido para facilitar a entrega de comida de diversos restaurantes. O app oferece uma interface intuitiva e funcionalidades essenciais como cadastro, login, visualização de restaurantes, carrinho de compras, checkout, atualização de conta e exclusão de conta. O objetivo principal do Vida Saborosa é promover a economia local e a sustentabilidade, alinhando-se com os Objetivos de Desenvolvimento Sustentável (ODS) da ONU, especialmente o ODS 2: Fome Zero e Agricultura Sustentável.

## Funcionalidades Principais

### 1. Cadastro de Usuário
- *Objetivo*: Permitir que novos usuários se cadastrem na plataforma.
- *Utilizador*: Novos usuários.
- *Resultado*: Usuário registrado com sucesso.
- *Apresentação*: Mensagem de confirmação.

### 2. Login de Usuário
- *Objetivo*: Permitir que usuários existentes façam login no app.
- *Utilizador*: Usuários existentes.
- *Resultado*: Usuário autenticado com sucesso.
- *Apresentação*: Mensagem de confirmação e redirecionamento para a tela principal.

### 3. Visualização de Restaurantes Disponíveis
- *Objetivo*: Mostrar uma lista de restaurantes cadastrados no app.
- *Utilizador*: Todos os usuários.
- *Resultado*: Lista de restaurantes exibida.
- *Apresentação*: Lista de restaurantes em formato de texto.

### 4. Detalhes do Restaurante
- *Objetivo*: Mostrar informações detalhadas sobre um restaurante selecionado.
- *Utilizador*: Usuários que desejam mais informações.
- *Resultado*: Detalhes exibidos.
- *Apresentação*: Informações em formato de texto.

### 5. Carrinho de Compras
- *Objetivo*: Exibir os itens adicionados pelo usuário ao carrinho.
- *Utilizador*: Usuários que desejam revisar suas compras.
- *Resultado*: Itens do carrinho exibidos.
- *Apresentação*: Lista de itens em formato de texto.

### 6. Checkout
- *Objetivo*: Permitir que o usuário finalize sua compra.
- *Utilizador*: Usuários que desejam concluir suas compras.
- *Resultado*: Compra finalizada com sucesso.
- *Apresentação*: Mensagem de confirmação.

### 7. Atualização de Conta
- *Objetivo*: Permitir que o usuário atualize suas informações.
- *Utilizador*: Usuários que desejam alterar suas informações.
- *Resultado*: Informações atualizadas.
- *Apresentação*: Mensagem de confirmação.

### 8. Exclusão de Conta
- *Objetivo*: Permitir que o usuário exclua sua conta.
- *Utilizador*: Usuários que desejam encerrar sua conta.
- *Resultado*: Conta excluída com sucesso.
- *Apresentação*: Mensagem de confirmação.

## Como Executar o Projeto

### Pré-requisitos

- Python 3.x
- Tkinter (geralmente incluído com a instalação padrão do Python)

### Instalação e Execução

1. Clone este repositório:
   ```sh
   git clone https://github.com/fernvndez/vidasaborosa.git

	2.	Navegue até o diretório do projeto:

cd vidasaborosa


	3.	Execute o script Python:

python app.py



Melhores Partes do Código e Diferenciais

1. Cadastro de Usuário

O código para o cadastro de usuários é simples e eficiente, permitindo a fácil adição de novos usuários.

def register_user(username, password):
    users.append({'username': username, 'password': password})
    messagebox.showinfo("Cadastro", "Usuário cadastrado com sucesso!")

2. Interface de Login

O login é seguro e direto, garantindo que apenas usuários autenticados possam acessar o sistema.

def login(username, password):
    for user in users:
        if user['username'] == username and user['password'] == password:
            messagebox.showinfo("Login", "Login realizado com sucesso!")
            return True
    messagebox.showerror("Login", "Nome de usuário ou senha incorretos.")
    return False

3. Visualização de Restaurantes

A visualização de restaurantes é clara e permite que o usuário veja facilmente as opções disponíveis.

def view_restaurants():
    restaurant_list = "\n".join([restaurant['name'] for restaurant in restaurants])
    messagebox.showinfo("Restaurantes Disponíveis", restaurant_list)

4. Carrinho de Compras e Checkout

O carrinho de compras é fácil de usar e o processo de checkout é simples, garantindo uma boa experiência ao usuário.

def view_cart():
    cart_items = "\n".join(cart)
    messagebox.showinfo("Carrinho", f"Items no carrinho:\n{cart_items}")

def checkout():
    if cart:
        messagebox.showinfo("Checkout", "Compra finalizada com sucesso!")
        cart.clear()
    else:
        messagebox.showwarning("Checkout", "Seu carrinho está vazio.")

5. Atualização e Exclusão de Conta

Permite que os usuários mantenham suas informações atualizadas e excluam suas contas se desejarem.

def update_account(old_username, new_username, new_password):
    for user in users:
        if user['username'] == old_username:
            user['username'] = new_username
            user['password'] = new_password
            messagebox.showinfo("Atualização", "Conta atualizada com sucesso!")
            return
    messagebox.showerror("Atualização", "Usuário não encontrado.")

def delete_account(username):
    global users
    users = [user for user in users if user['username'] != username]
    messagebox.showinfo("Exclusão", "Conta excluída com sucesso!")

Estrutura do Código

O arquivo principal app.py contém toda a lógica do aplicativo, desde a interface do usuário até as funções de manipulação de dados.

Funcionalidade do Código

O código inclui funções para:

	•	Cadastrar Usuário: register_user
	•	Login de Usuário: login
	•	Atualizar Conta: update_account
	•	Excluir Conta: delete_account
	•	Visualização de Restaurantes: view_restaurants
	•	Detalhes do Restaurante: view_restaurant_details
	•	Carrinho de Compras: view_cart
	•	Checkout: checkout

Contribuição

Contribuições são bem-vindas! Se você tiver sugestões de melhorias, por favor, faça um fork do repositório e envie um pull request.

Licença

Distribuído sob a licença MIT. Veja LICENSE para mais informações.

Contato

Leonardo Fernandez - @fernvndezsb - leonardofernandezcontato@gmail.com

Link do Projeto: https://github.com/fernvndez/vidasaborosa-app

Este README inclui todas as informações necessárias sobre o aplicativo, desde a descrição do projeto até as funcionalidades, melhores partes do código, como executar o projeto, e informações sobre contribuição e licença. Certifique-se de substituir seuusuario e seuemail@dominio.com com suas informações reais antes de publicar.
