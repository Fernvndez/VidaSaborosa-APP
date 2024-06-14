# VidaSaborosa-APP

## Descrição do Projeto
VidaSaborosa é um aplicativo de entrega de comida que facilita a conexão entre restaurantes e clientes, proporcionando uma experiência de pedido de refeições rápida e eficiente. Este projeto simula as funcionalidades básicas de um aplicativo de entrega, incluindo cadastro, login, visualização de restaurantes, carrinho de compras e checkout.

## Funcionalidades Principais
1. *Cadastro de Usuário*
   - Permite que novos usuários se registrem no aplicativo.
   - Armazena os dados do usuário em um arquivo de texto para persistência de dados.

2. *Login de Usuário*
   - Autentica usuários registrados, permitindo o acesso ao sistema.

3. *Visualização de Restaurantes*
   - Exibe uma lista de restaurantes disponíveis.
   - Permite ao usuário visualizar detalhes específicos de cada restaurante.

4. *Carrinho de Compras e Checkout*
   - Mostra os itens adicionados pelo usuário ao carrinho.
   - Permite a finalização da compra com opções de pagamento.

## Tecnologias Utilizadas
- Python 3.x
- Interface gráfica com Tkinter
- Persistência de dados com arquivos de texto (.txt)

## Instruções de Instalação
1. Clone o repositório:
    bash
    git clone https://github.com/fernvndez/VidaSaborosa-APP.git
    cd VidaSaborosa-APP
    

2. Instale as dependências necessárias (no caso, Tkinter):
    bash
    pip install tk
    

3. Execute o aplicativo:
    bash
    python app.py
    

## Estrutura do Projeto

VidaSaborosa-APP/
│
├── data/
│   ├── users.txt        # Armazena dados dos usuários
│   ├── restaurants.txt  # Dados fictícios dos restaurantes
│   └── orders.txt       # Armazena pedidos realizados
│
├── assets/
│   ├── logo.png         # Logotipo do aplicativo
│   └── sample-images/   # Imagens de amostra de pratos e restaurantes
│
├── app.py               # Arquivo principal do aplicativo
├── README.md            # Documentação do projeto
└── requirements.txt     # Lista de dependências do projeto

## Destaques do Código
### Cadastro de Usuário
```python
def register_user():
    with open('data/users.txt', 'a') as file:
        file.write(f"{username},{password}\n")

Esta função permite que novos usuários sejam registrados no sistema e seus dados sejam salvos em um arquivo de texto.

Login de Usuário

def login_user():
    with open('data/users.txt', 'r') as file:
        users = file.readlines()
        for user in users:
            stored_username, stored_password = user.strip().split(',')
            if stored_username == username and stored_password == password:
                return True
    return False

A função de login autentica usuários comparando as credenciais fornecidas com as armazenadas no arquivo.

Visualização de Restaurantes

def view_restaurants():
    with open('data/restaurants.txt', 'r') as file:
        restaurants = file.readlines()
        for restaurant in restaurants:
            print(restaurant.strip())

Esta função lê e exibe a lista de restaurantes disponíveis a partir de um arquivo de texto.

Contribuição

	1.	Faça um fork do projeto.
	2.	Crie uma branch para sua funcionalidade (git checkout -b feature/nova-funcionalidade).
	3.	Faça commit de suas alterações (git commit -m 'Adiciona nova funcionalidade').
	4.	Faça push para a branch (git push origin feature/nova-funcionalidade).
	5.	Abra um Pull Request.

Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

Contato

Para mais informações, entre em contato via email leonardofernandezcontato@gmail.com
