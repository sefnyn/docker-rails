# docker-rails

These five files (plus two config files) can be used to build a complete rails app running on port 8000.

Instructions are based on those on the Docker web site.

1. Install docker and docker compose
2. docker-compose run web rails new . --force --no-deps --database=postgresql  [**IGNORE WARNINGS ABOUT YARN**]
3. ls command to inspect new files
4. sudo chown -R $USER:$USER .
5. docker-compose build
6. cp database.yml config/database.yml
7. cp webpacker.yml config/webpacker.yml  [**BUG FIX**] 
8. docker-compose up
9. In a new terminal enter: docker-compose run web rake db:create
10. browse to localhost:8000
