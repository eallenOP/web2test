# PHP on Windows instructions

1. Make a project folder somewhere
2. Download the zip of the right version of PHP (mine came from http://windows.php.net/download/ but yours might come from the I: drive, or this repo)
3. Unzip it into your project folder and shorten the name to `php-7`
4. Make a file in your project folder called `index.php` and paste into it `<?php phpinfo();?>`
5. Open a terminal window and navigate to your project folder
6. Type in `php-7\php.exe -S localhost:8000`
7. Open a web browser and point it to `localhost:8000` and you should see your PHP info page
8. Go back and find out where you went wrong, or give the person next to you a high five