# API Laravel

## Requisitos

-   PHP 8.0+
-   Composer
-   MySQL

## Instalação

1. Clone o repositório:

    ```bash
    git clone https://github.com/williammeier/api-laravel.git
    cd api-laravel
    ```

2. Instale as dependências:

    ```bash
    composer install
    ```

3. Configure o arquivo `.env` com suas credenciais de banco de dados.

4. Execute as migrações:

    ```bash
    php artisan migrate
    ```

5. Gere a chave JWT:

    ```bash
    php artisan jwt:secret
    ```

6. Inicie o servidor:
    ```bash
    php artisan serve
    ```

## Uso

### Autenticação

-   Registro:

    ```bash
    POST /api/register
    {
        "name": "Seu Nome",
        "email": "seuemail@example.com",
        "password": "sua_senha",
        "password_confirmation": "sua_senha"
    }
    ```

-   Login:
    ```bash
    POST /api/login
    {
        "email": "seuemail@example.com",
        "password": "sua_senha"
    }
    ```

### Endpoints

-   Listar todos os itens:

    ```bash
    GET /api/products
    ```

-   Buscar item por ID:
    ```bash
    GET /api/products/{id}
    ```

### Documentação

A documentação da API está disponível em `/api/documentation`.

## Testes

Para executar os testes, use o comando:

```bash
php artisan test
```
