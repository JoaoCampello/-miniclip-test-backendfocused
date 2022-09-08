# João Campello: miniclip-test-backendfocused

## Project Prerequisites

- Install composer
- Install Docker-compose in your linux distribution
- If you don't have the JSON keyfile, activate Cloud vision in your google account and create new key for the project, download it and copy it as key.json into project root directory.

PS: you can create "sail" alias

## Project setup
```bash
$ composer install
```
```bash
$ ./vendor/bin/sail npm install
```
```bash
$ cp .env.example .env
```
```php
$ ./vendor/bin/sail artisan key:generate
```
```php
$ ./vendor/bin/sail artisan migrate
```
```php
$ ./vendor/bin/sail artisan storage:link
```
```php
$ ./vendor/bin/sail npm run dev
```
to generate swagger documentation:
```php
$ ./vendor/bin/sail artisan l5-swagger:generate
```
to build and run containers execute:
```php
$ ./vendor/bin/sail up
```
If apache2 is running on port 80 run ```sudo service apache2 stop``` before trying again

# **API Routes**
### All API routes with Schema and examples are available on http://localhost/api/docs
![API documentation](public/swagger2.png?raw=true "How API documentation is look")
<br>
<br>
**You can click on try it to test any of the routes**
<br>
<br>

# **User Interface**
![Example Reports list](public/report-list-2.png?raw=true "Example Reports list sort by decreasing probability")

## Callback

- Here http://localhost/api/callback-test is the callback example that i have implement, you can add it as image report callback but your endpoint must be an online endpoint. (like https url)
