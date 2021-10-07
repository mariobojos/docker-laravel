# docker-laravel

This project are pre-configured docker containers geared towards Laravel 8 web development.

## Folder structure:
<pre>
/ (root folder)
|
|--/nginx (web server configurations)
|--/mysql (MySQL-related files)
|--/src (this is where Laravel framework is installed)
</pre>

## Installation
- Clone repo
- In the CLI run $<code>docker-compose --build -d </code>
- Copy the <em>src/.env.example</em> to .env file
- Edit the contents of the .env file with:
<pre>
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret
</pre>
- Create an alias for <em>artisan</em>: <code>$ alias artisan="docker-compose exec php php /var/www/html/artisan"</code>
- Refresh bash or zsh: 
  <pre>
  $ source ~/.bashrc -OR-
  $ source ~/.zshrc
  </pre>
- Run migrations: $<code>artisan migrate:fresh</code>
- Visit url: <pre>http://localhost:8088 </pre>
- You can begin coding. Get to it!

### Note 1:
- Be sure to shutdown the docker containers after you end your coding session by
<pre>$ docker-compose down</pre>

### Note 2:
- You can change the port numbers in docker-compose.yml file.
- Restart the containers with <code>$ docker-compose restart</code>


## Source
Project was based on a video tutorial uploaded in YouTube: https://www.youtube.com/watch?v=5N6gTVCG_rw.

