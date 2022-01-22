# Swagger\Client\TagsApi

All URIs are relative to *https://api.fulfilling.io/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tagsGet**](TagsApi.md#tagsget) | **GET** /tags | 

# **tagsGet**
> \Swagger\Client\Model\Tags tagsGet()



Obtém todas as etiquetas disponíveis na plataforma (não-implementado)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_key', 'Bearer');// Configure API key authorization: api_secret
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');

$apiInstance = new Swagger\Client\Api\TagsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->tagsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TagsApi->tagsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Tags**](../Model/Tags.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

