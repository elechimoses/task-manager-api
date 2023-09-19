
# Task Manager API 




## Installation


1. Clone the repository:
```bash
  git clone https://github.com/elechimoses/task-manager-api.git 
```

2. Navigate to the project directory:
   
```bash
  cd my-project
```
3. Install PHP dependencies using Composer:

 ```bash
    composer install
```
4. Copy the `.env.example` file to `.env` and configure your database and other environment settings:
   
 ```bash
  cp .env.example .env
```

5. Generate the application key:
```bash
  php artisan key:generate
```
6. Run database migrations:
```bash
   php artisan migrate
```
7. Start the development server:
```bash
   php artisan serve
```
8. Access your app in a web browser at `http://localhost:8000`.


    


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

