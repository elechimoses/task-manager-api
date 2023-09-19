
# Task Manager API 




## Installation



```bash
  git clone https://github.com/yourusername/your-app.git

  cd my-project

  composer install

  cp .env.example .env

  php artisan key:generate

  php artisan migrate
```
    


## Usage/Examples




## API Endpoints

`api/register` (POST) 

User registeration.

Request:
```php
{
  "name": "John Doe",
  "email": "user@example.com",
  "password": "secret_password"
}

```

Response (Success):
```php
{
 "message": "User registered successfully"
}

```

`api/login` (POST) 

Authenticate a user and recieve an Authentication token.

Request:
```php
{
  "email": "user@example.com",
  "password": "secret_password"
}

```

Response (Success):
```php
{
  "message": "Login successful",
  "token": "your_access_token_here"
}

```

Response (Error):
```php
{
 "errors": {
        "email": [
            "The email has already been taken."
        ],
        "password": [
            "The password field must be at least 6 characters."
        ]
    }
}
```

Response (Error):
```php
{
 "message": "Invalid credentials"
}

```

