1. `docker compose up -d`
2. `docker compose exec app bash`
3. `chmod -R 777 storage bootstrap/cache`
4. `composer install`
5. `cp src/.env.example src/.env`
6. `docker compose exec app bash`
7. `php artisan storage:link`
