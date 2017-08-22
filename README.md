# PHP on Windows instructions

1. Decide where to clone this to
2. Clone this repo
3. Open a terminal window and navigate into this repo (the web2test folder)
4. Type in `php-7\php.exe -S localhost:8000`
5. Open a web browser and point it to `localhost:8000` and you should see your PHP info page
6. Go back and find out where you went wrong, or give the person next to you a high five

Now you can put all your files to be tested straight into this web2test folder and you can navigate to them in the browser.

# MariaDB connection
## from built-in php server

In order to connect to a maria database, your PHP install needs to know where the driver is (needs the whole path(?)).
This is different for each person, so everyone will need to set it correctly in php.ini.

1. Find the line that states the path to the extension folder (search for `extension_dir`)	(Line 738 in my php.ini file)
2. Change the path to match where your extension folder is (inside your php-7 folder, so in my case `extension_dir = "H:\web2test\php-7\ext"` because the extension directory is called `ext`)

# Turning on linting in VS Code

Once you have your php built-in server working, you can enable linting (syntax error underlining) in VS Code. Unfortunately you have to set this up each time you log in to the deep freeze machines in class, but it's easy.

1. Open your web2test folder (with your work in it) in VS Code
2. Open the settings (Ctrl+, or File>Preferences>Settings)
3. Paste the following code into your user settings (the pane open on the right)

```  
  // Points to the PHP executable.
  "php.validate.executablePath": null,

  // Whether the linter is run on save or on type.
  "php.validate.run": "onType"
```
Now you should see syntax errors underlined with red zigzags!
