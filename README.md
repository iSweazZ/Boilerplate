


![Logo](https://laravel.com/images/home/video-preview-static.jpg)



# Boilerplate Laravel 12 + VueJS with Docker

## Introduction

Welcome to the Laravel 12 + Vue.js **Boilerplate**! This project serves as a starting point for developing modern web applications. It combines the powerful backend capabilities of Laravel with the dynamic frontend of Vue.js, offering a seamless development experience.

## Features

- **Laravel 12**: Backend framework with built-in routing, authentication, and ORM (Eloquent).
- **Vue.js**: Reactive JavaScript framework for building dynamic user interfaces.
- **Dockerized Environment**: Preconfigured containers for:
    - Laravel backend
    - Vue.js frontend
    - PostgreSQL database

## Prerequisites

Make sure you have the following installed:
- [Docker](https://www.docker.com/)
- Docker Compose

## Installation

1. Clone the repository:
```
git clone https://github.com/iSweazZ/boilerplate.git
cd Boilerplate
```
2. Start the Docker containers:
```
docker-compose up -d --build
```

3.Install backend dependencies:
```
docker-compose exec app composer install
```

4. Install frontend dependencies:
```
docker-compose exec app npm install
```

5. Generate the application key:
```
docker-compose exec app php artisan key:generate
```

6. Run migrations:
```
docker-compose exec app php artisan migrate
```

## Usage

### Development

Access the application in your browser:

* Laravel Backend: http://localhost:9000
* Frontend served via Nginx: http://localhost:8080

### Database Access

* MySQL: Accessible on port ```3306``` (map to a different port if needed).

### Production

```
docker-compose exec app npm run build
```
