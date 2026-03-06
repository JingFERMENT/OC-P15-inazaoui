# Optimization of a Photography Portfolio Website

## Project description

Ina Zaoui is a photography portfolio web application developed with Symfony. 

The application provides:
- a **front office** where visitors can explore the portfolio;
- a **back office** where the administrator can manage albums, media, and guest accounts, and where **guest photographers** can manage their own media.

## Improvements implemented

This project focused on modernizing, securing, and improving the existing application.  
The following enhancements have been implemented:

- migrated the project from **Symfony 5.4** to **Symfony 7.4 (LTS)**
- secured media uploads through file validation and safer authentication-related data handling
- implemented **guest account management**, including email invitations and password setup
- improved performance by reducing **N+1 queries**, compressing images, and minifying CSS files
- strengthened code quality with **automated tests and static analysis tools**
- provided clear **technical documentation** for future developers
- set up a **continuous integration pipeline**.

---

## Technical Stack

<p>
  <img src="https://img.shields.io/badge/PHP-8.4-777BB4?style=flat-square&logo=php&logoColor=white" alt="PHP">
  <img src="https://img.shields.io/badge/Symfony-7.4-000000?style=flat-square&logo=symfony&logoColor=white" alt="Symfony">
  <img src="https://img.shields.io/badge/PostgreSQL-16-336791?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Doctrine-ORM%203.x-FC6A31?style=flat-square&logo=doctrine&logoColor=white" alt="Doctrine ORM">
  <img src="https://img.shields.io/badge/Twig-3.x-85EA2D?style=flat-square&logo=twig&logoColor=black" alt="Twig">
  <img src="https://img.shields.io/badge/Docker-Containerized-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/GitHub%20Actions-CI-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions">
</p>

### Development and Code Quality Tools

<p>
  <img src="https://img.shields.io/badge/PHPUnit-Tests-6C3483?style=flat-square" alt="PHPUnit">
  <img src="https://img.shields.io/badge/PHPStan-Static%20Analysis-4B32C3?style=flat-square" alt="PHPStan">
  <img src="https://img.shields.io/badge/PHP%20CS%20Fixer-Code%20Style-8A2BE2?style=flat-square" alt="PHP CS Fixer">
</p>

### Key Dependencies

<p>
  <img src="https://img.shields.io/badge/Symfony%20Mailer-Mailer-000000?style=flat-square&logo=symfony&logoColor=white" alt="Symfony Mailer">
  <img src="https://img.shields.io/badge/LiipImagineBundle-Images-4CAF50?style=flat-square" alt="LiipImagineBundle">
  <img src="https://img.shields.io/badge/SensioLabs%20Minify-Minify-FF9800?style=flat-square" alt="SensioLabs Minify Bundle">
  <img src="https://img.shields.io/badge/Zenstruck%20Foundry-Foundry-009688?style=flat-square" alt="Zenstruck Foundry">
  <img src="https://img.shields.io/badge/DAMA%20Doctrine-Test%20Bundle-3F51B5?style=flat-square" alt="DAMA Doctrine Test Bundle">
  <img src="https://img.shields.io/badge/Doctrine%20Fixtures-Fixtures-FC6A31?style=flat-square&logo=doctrine&logoColor=white" alt="Doctrine Fixtures Bundle">
</p>

---

## Prerequisites

- PHP : 8.2+
- Composer
- Symfony CLI
- PostgreSQL: 16+

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/JingFERMENT/OC-P15-inazaoui
cd OC-P15-inazaoui
```

### 2. Install dependencies
```bash
compose install 
```

### 3. Configure environment variables

Create or update your .env.local file with your local configuration:

```bash
DATABASE_URL="postgresql://username:password@127.0.0.1:5432/ina_zaoui?serverVersion=16&charset=utf8"
MAILER_DSN=null://null
```

- `DATABASE_URL`: configure with your PostgreSQL credentials
- `MAILER_DSN`: configure with your mail service, or keep `null://null` to disable emails in development

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
## PERFORMANCE IMPROVEMENTS

### Guests page
![Guests Page Before](docs/Guests_page_performance_before.png)
## Improve the query
### Add CACHE
### Add Paginations 
### Minfiy the css file
### Compress the images from jpg to webp





## CONTRIBUTION 
To contribute to this project, please read [CONTRIBUTING.md](CONTRIBUTING.md).


