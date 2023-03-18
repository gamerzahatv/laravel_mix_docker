not login php myadmin  wait phpmyadmin gen data file finish   and login 
after gen mysql data finish    use command 

docker compose build
docker compose up -d
(fi you want to stop container )   : docker compose down
docker compose exec app composer create-project --prefer-dist laravel/laravel .
docker compose exec app php artisan key:generate
docker compose exec app php artisan storage:link
docker compose exec app chmod -R 777 storage bootstrap/cache
docker compose exec app php artisan migrate
docker compose exec app php artisan permission:create-role admin
docker compose exec app php artisan permission:create-role User