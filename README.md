# Sublime text 3
Sublime text 3 snippets, package and preferences

## Configuration

##### Sublime PHP CS Fixer

Install php-cs-fixer directly with composer by running:

    composer global require friendsofphp/php-cs-fixer

Also you can create a config file `$HOME/.phpcsfixer`

    <?php
    return PhpCsFixer\Config::create()
    ->setRules([
        '@Symfony' => true,
        'array_syntax' => ['syntax' => 'short'],
        'no_unused_imports' => true,
    ]);

If you've created a config file, you have to configure its path in the plugin's settings.
In Menu->Preferences -> Package Settings -> PHP CS Fixer -> Settings - User

    {
        "config": "/path/to/.phpcsfixer"
    }

Please note that this plugin don't try to find the config file automatically. If you want to create a config file, you have to specify its path in the plugin settings. Although you can configure the rules directly on your plugin settings, it's recommended to create the config file, as it's easier to configure every rule than using the 'rules' directive in the plugin settings.

##### PHP_CodeSniffer
Install PHP_CodeSniffer directly with composer by running:

    composer global require "squizlabs/php_codesniffer=*"
