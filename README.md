# SwaggerClient-php
The Conversions API (for web) allows advertisers to send web events from their servers directly to Facebook. Conversions API events are linked to a pixel and are processed like browser pixel events. This means that these conversion events are used in measurement, reporting, and optimization in the same way as browser pixel events.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: facebook_api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\EventRequest(); // \Swagger\Client\Model\EventRequest | Facebook Conversions API (for Web) post request
$pixel_id = "pixel_id_example"; // string | 

try {
    $result = $apiInstance->pixelIdEventsPost($body, $pixel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->pixelIdEventsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://graph.facebook.com/v8.0*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**pixelIdEventsPost**](docs/Api/DefaultApi.md#pixelideventspost) | **POST** /{pixelId}/events | 

## Documentation For Models

 - [Content](docs/Model/Content.md)
 - [CustomData](docs/Model/CustomData.md)
 - [Event](docs/Model/Event.md)
 - [EventRequest](docs/Model/EventRequest.md)
 - [ResponseError](docs/Model/ResponseError.md)
 - [ResponseErrorError](docs/Model/ResponseErrorError.md)
 - [ResponseSuccess](docs/Model/ResponseSuccess.md)
 - [UserData](docs/Model/UserData.md)

## Documentation For Authorization


## facebook_api_key

- **Type**: API key
- **API key parameter name**: access_token
- **Location**: URL query string


## Author

web_signals_integrations@fb.com

