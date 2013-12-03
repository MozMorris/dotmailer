DotMailer
=========

A php class to interact with the dotMailer API. In order to use this class you will need an account (with API access) from dotMailer (http://www.dotmailer.com).

Install via Composer
--------------------

    "repositories": [
      {
        "type": "vcs",
        "url": "https://github.com/MozMorris/dotmailer.git"
       }
    ],
    "require": {
      "MozMorris/dotmailer": "dev-dev"
    },

And then...

    $ composer install

Usage
-----

To get up and running just provide the class with your API username and password;

    $dotmailer = new DotMailer\DotMailer('username', 'password');

You can then interact with the methods using the same method names as described in the [API documentation](http://www.dotmailer.co.uk/api/). For example to list all address books on your account just use the following

    $addressBooks = $dotmailer->ListAddressBooks();

    foreach ($addressBooks as $book) {
    	print $book->ID  . ' => ' . $book->Name . PHP_EOL;
    }
