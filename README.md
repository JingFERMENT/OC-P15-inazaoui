# Optimization of Ina Zaoui’s Photography Portfolio Website

![PHP](https://img.shields.io/badge/PHP-8.4-blue)
![Symfony](https://img.shields.io/badge/Symfony-7.4-black)
![Tests](https://img.shields.io/badge/tests-PHPUnit-green)
![Docker](https://img.shields.io/badge/Docker-enabled-blue)

## Project description

Ina Zaoui is a photography portfolio web application developed with Symfony. 
The project aims to modernize and improve an existing website used to showcase landscape photography from around the world.

## Project objectives 
  - improve application security and maintainability 
  - migrate the application to a more recent version
  - secure media uploads
  - implement new features (ex: guest account management)
  - optimize page performance
  - add automated tests
  - write a documentation for future developers
  - implement a continuous integration pipeline.

---

## Technical Stack

- **Language:** PHP 8.4
- **Framework:** Symfony 7.4
- **Database:** PostgreSQL 16
- **ORM:** Doctrine ORM 3.x
- **Templating Engine:** Twig 3.x
- **Containerization:** Docker
- **Continuous Integration:** GitHub Actions

### Development and Code Quality Tools

- **PHPUnit** for automated testing
- **PHPStan** for static analysis
- **PHP CS Fixer** for coding standards

### Key Dependencies

- **Symfony Mailer**
- **LiipImagineBundle**
- **SensioLabs Minify Bundle**
- **Zenstruck Foundry**
- **DAMA Doctrine Test Bundle**
- **Doctrine Fixtures Bundle**

---

## Prerequisites

- PHP : >8.2
- Composer
- Symfony CLI
- PostgreSQL

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/JingFERMENT/OC-P15-inazaoui
cd OC-P15-inazaoui
```

### 2. Install dependencies
```bash
compse install 
```

### 3. Configure environment variables

Create or update your .env.local file with your local configuration:

DATABASE_URL="postgresql://username:password@127.0.0.1:5432/ina_zaoui?serverVersion=16&charset=utf8"

MAILER_DSN=null://null

### 4. Create the database
```bash
php bin/console doctrine:database:create
```

### 5. Run migrations
```bash
php bin/console doctrine:migrations:migrate
```

### 6. Load fixtures
```bash
php bin/console doctrine:fixtures:load
```

## How to install and run the project

Start the Symfony server

```bash
symfony server:start
```

Then open your browser and go to:
http://127.0.0.1:8000


## USAGE
The application contains two main parts:

### Front Office

The front office is the public part of the website.
Visitors can browse the portfolio pages and discover Ina Zaoui’s photography work.

### Back Office / Admin

The admin area allows authenticated users to manage content. It Depends on the role:

- **Admin** can manage albums, all media, and guests,
- **Guests** can only access and manage their own media.

### Main features include:

- viewing albums and media
- uploading images
- managing guest accounts
- blocking or deleting guests
- accessing guest pages. 

### Tests
The project requires a code coverage report above 70%.

Run PHPUnit tests
```bash
php bin/phpunit
```

Run tests with coverage
```bash
php bin/phpunit --coverage-html var/coverage
```

After running this command, open the coverage report in:
```bash
open var/coverage/index.html
```

Run quality commands
PHPStan:
```bash
vendor/bin/phpstan analyse
```
PHP CS Fixer:
```bash
vendor/bin/php-cs-fixer fix
```

Contribute to the project
CONTRIBUTING.md


