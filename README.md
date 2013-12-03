DotMailer
=========

A php class to interact with the dotMailer API. In order to use this you'll need a [dotMailer](http://www.dotmailer.com/) account with API access.

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

Instantiate the class with your API username and password:

    $dotmailer = new DotMailer\DotMailer('username', 'password');

Then use the `$dotmailer` object to interact with the [API](http://www.dotmailer.co.uk/api/) using the same method names as described in the [documentation](http://www.dotmailer.co.uk/api/). 

Example
-------

List address books:

    $addressBooks = $dotmailer->ListAddressBooks();
    foreach ($addressBooks as $book) {
    	print $book->ID  . ' => ' . $book->Name . PHP_EOL;
    }
