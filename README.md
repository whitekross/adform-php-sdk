# AdForm SDK for PHP

The **AdForm SDK for PHP** to access [AdForm's API](http://api.adform.com/help/)

### Installation
Use [Composer] to download dependencies:

```
$ composer install
```

### Usage
```
$api = new ApiFactory(new HttpClient);
$ticket = $api->auth('<username>', '<password>');
$result = $api->call(ApiFactory::ADVERTISERS, $ticket, ['Names' => '<name-filter>']);
```

### Examples
Same code examples are located in the "examples" dir.
Find and rename config.php.dist to config.php and edit with your AdForm credentials.
Finally run with:
```
$ php examples/advertisers.php
```


### Endpoints
Currently implemented Endpoints:
* [Authentication](http://api.adform.com/help/references/buyer-solutions/account/authentication/login)
* [Advertisers](http://api.adform.com/help/references/buyer-solutions/advertiser/management/get-advertisers)
* [Campaigns](http://api.adform.com/help/references/buyer-solutions/campaign)
* [Users](http://api.adform.com/help/references/buyer-solutions/account/users/get-users)
* [Reporting Stats](http://api.adform.com/help/references/buyer-solutions/reporting/stats)
* [Data Export](http://api.adform.com/help/references/buyer-solutions/reporting/data-exports)

### Run Tests
```
$ ./vendor/bin/phpunit
```