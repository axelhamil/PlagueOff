# Simple MVC

"Plague Off" uses some cool APIs as FOAAS or complimentr. 

### Check on Travis

1. Go on [https://travis-ci.com](https://travis-ci.com).
2. Sign up if you don't have account,
3. Look for your project in search bar on the left,
4. As soon as your repository have a `.travis.yml` in root folder, Travis should detect it and run test.
5. Configure Travis as described in the screenshot below, this is needed to avoid performance issues.

### Configure you repository - Settings options

1. Add your students team as contributor .
2. Disallow both on 'dev' and 'master' branches your students writing credentials. 
3. Disallow merge available while one approbation is not submitted on PR.

> You can watch this very tiny short video : (Loom : verrouillage branches GitHub)[https://www.loom.com/share/ad0c641d0b9447be9e40fa38a499953b]

## Steps

1. Clone the repo from Github.
2. Run `composer install`.
3. Create *config/db.php* from *config/db.php.dist* file and add your DB parameters. Don't delete the *.dist* file, it must be kept.
```php
define('APP_DB_HOST', 'your_db_host');
define('APP_DB_NAME', 'your_db_name');
define('APP_DB_USER', 'your_db_user_wich_is_not_root');
define('APP_DB_PWD', 'your_db_password');
```
4. Run the internal PHP webserver with `php -S localhost:8000 -t public/`. The option `-t` with `public` as parameter means your localhost will target the `/public` folder.
5. Go to `localhost:8000` with your favorite browser.
6. Tell people to back off.

### Windows Users

If you develop on Windows, you should edit you git configuration to change your end of line rules with this command :

`git config --global core.autocrlf true`

## APIs
* https://www.foaas.com/
* https://official-joke-api.appspot.com
* https://complimentr.com/api
* http://api.voicerss.org/

## URLs availables

* Home page at [localhost:8000/](localhost:8000/)
* Info page at [localhost:8000/plagueOff/info](localhost:8000/plagueOff/info)
