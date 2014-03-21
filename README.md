Eventbrite API Connector
========================

[![Build Status](https://travis-ci.org/dcsg/EventbriteApiConnector.png?branch=master)](https://travis-ci.org/dcsg/EventbriteApiConnector) [![Latest Stable Version](https://poser.pugx.org/dcsg/eventbrite-api-connector/v/stable.png)](https://packagist.org/packages/dcsg/eventbrite-api-connector) [![Total Downloads](https://poser.pugx.org/dcsg/eventbrite-api-connector/downloads.png)](https://packagist.org/packages/dcsg/eventbrite-api-connector) [![Latest Unstable Version](https://poser.pugx.org/dcsg/eventbrite-api-connector/v/unstable.png)](https://packagist.org/packages/dcsg/eventbrite-api-connector) [![License](https://poser.pugx.org/dcsg/eventbrite-api-connector/license.png)](https://packagist.org/packages/dcsg/eventbrite-api-connector)  [![Scrutinizer Quality Score](https://scrutinizer-ci.com/g/dcsg/EventbriteApiConnector/badges/quality-score.png?s=1a8f2259185123eb812dd489793c22c5d7cdb641)](https://scrutinizer-ci.com/g/dcsg/EventbriteApiConnector/) [![Code Coverage](https://scrutinizer-ci.com/g/dcsg/EventbriteApiConnector/badges/coverage.png?s=90d3ce083a76083f6dcbeed1cdd74dd0874e2c66)](https://scrutinizer-ci.com/g/dcsg/EventbriteApiConnector/) [![SensioLabsInsight](https://insight.sensiolabs.com/projects/159123de-9d05-4af3-a650-6e8ea7aadaea/mini.png)](https://insight.sensiolabs.com/projects/159123de-9d05-4af3-a650-6e8ea7aadaea)

Eventbrite Api Connector is a lightweight PHP 5.3 library for issuing the Eventbrite API.

### Instalation

#### Composer

```json
"require": {
    ...
    "dcsg/eventbrite-api-connector": "dev-master"
}
```

### Usage

```php
<?php

require __DIR__ . '/path/to/vendor/autoload.php';

use EventbriteApiConnector\Eventbrite;
use EventbriteApiConnector\HttpAdapter\BuzzHttpAdapter;

$apiKeys = array(
    'app_key' => 'YOUR APP KEY'
);

$params = array(
    'keywords' => 'php'
);

$eventbrite = new Eventbrite(new BuzzHttpAdapter(), $apiKeys);
$results = $eventbrite->get('event_search', $params);
```

### TODO

 * Implement more HTTP Adapters
 * Implement OAuth2.
 * Add documentation.

### Credits

 * [Daniel Gomes](https://github.com/dcsg)
 * Http Adapters inspired by [Geocoder PHP Library](https://github.com/geocoder-php/Geocoder)

### License

**Eventbrite API Connector** is released under the MIT License. See the bundled LICENSE file for details.
