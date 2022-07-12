# luu tru databse
mkdir mysql
cd mysql
mkdir db
cd ../
# build project
docker-compose build
docker-compose up -d

# build laravel
docker exec -it laravel bash <br>
composer install
chmod -R 775 storage bootstrap/cache
chmod o+w ./storage/ -R
cp .env.example .env
php artisan key:generate
# url laravel
localhost:8080 
# url reactjs
localhost:8030 
# url phpmyadmin
localhost:8081 
# merge
test merges dev
