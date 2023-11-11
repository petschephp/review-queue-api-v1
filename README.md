ReviewQueue V1
=========================



### Documentation
https://developers.reviewqueue.net


### Installation
This library can be found on Packagist. The recommended way to install this is through [composer](http://getcomposer.org)

```shell
composer install require local-spark/reviewqueue-v1

```


### Example

```php
require 'vendor/autoload.php';
$reviewQueueApi = new ReviewQueueV1('<YOUR_API_KEY>');

```

### Send Review Request
```php

// Send a review request
$reviewRequest = $reviewQueueApi->reviewRequest();
$response = $reviewRequest->create('+18888888888');


print_r($reviewRequest->client->headers['X-Rate-Limit-Limit']);
echo $reviewRequest->client->responseCode;

```