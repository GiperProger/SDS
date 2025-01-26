# Symfony Docker Skeleton

A **lightweight, ready-to-use Symfony 6+ skeleton** with **Docker Compose** for local development. This project provides a quick start for creating a modern PHP application with a clean, containerized infrastructure.
If you want to replace Symfony version or change the framework completely, just put your source code into app folder  

![Symfony Version](https://img.shields.io/badge/Symfony-6.x-brightgreen.svg?style=flat-square)
![PHP Version](https://img.shields.io/badge/PHP-8.2-blue.svg?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)

> **Keywords**: symfony, docker, php, skeleton, boilerplate, mysql, phpmyadmin, docker-compose, psalm, nginx, php-fpm

## Table of Contents
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Contacts](#contacts)

---

## Features

- **Symfony 6+**: Modern framework for building robust PHP applications.
- **PHP 8.2-FPM** container: Runs your application code in a separate container.
- **Nginx** container: Serves your app on `localhost:8080`.
- **MySQL 8** container: Persistent database volume.
- **phpMyAdmin** container: Manage your database on `localhost:8081`.
- **Docker-First Approach**: All configs in a `docker/` directory, ensuring a clean separation between infrastructure and application code.

---
 
## Project Structure

```plaintext
├── app/
│   ├── config/
│   ├── public/
│   ├── src/
│   ├── tests/
│   ├── vendor/       # Ignored by Git
│   ├── composer.json
│   └── composer.lock
├── docker/
│   ├── nginx/
│   │   ├── Dockerfile
│   │   └── default.conf
│   ├── php/
│   │   ├── Dockerfile
│   │   └── php.ini
│   ├── mysql/
│   │   └── Dockerfile    # optional
│   ├── phpmyadmin/
│       └── Dockerfile    # optional
│   
├── .gitignore
├── docker-compose.yml
├── LICENSE
└── README.md
```

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/GiperProger/SDS.git
   cd SDS
   ```
2. **Create env files**

   ```plaintext
   in the root directory create .env file based on .env_example 
   in the app directory create .env file based on .env_example 
   ```   

3. **Build containers**

   ```bash
   docker-compose build
   ```
   
4. **Start services**
   ```bash
   docker-compose up -d
   ```
5. **Install Composer Dependencies**
   ```bash
   docker-compose exec php composer install -d /var/www/html/app
   ```
6. **Verify setup**
   - Visit http://localhost:8080 to check your Symfony app
   - Visit http://localhost:8081 to check PHPMyAdmin

---

## Contacts

- **Author**: Sergei Priadkin.
- **Email**: giperproger@gmail.com
- **GitHub**: https://github.com/GiperProger.
- **Telegram**: giperproger.


**Thank you!**  

If you have any suggestions or issues, please open an Issue or Pull Request.  
Happy coding!