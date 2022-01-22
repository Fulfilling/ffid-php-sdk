# Swagger\Client\ClientsApi

All URIs are relative to *https://api.fulfilling.io/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clientsGet**](ClientsApi.md#clientsget) | **GET** /clients | 
[**clientsPlansGet**](ClientsApi.md#clientsplansget) | **GET** /clients-plans | 
[**clientsPost**](ClientsApi.md#clientspost) | **POST** /clients | Apenas para clientes que tem autorização de criar clientes dentro de sua conta.

# **clientsGet**
> \Swagger\Client\Model\Clients clientsGet($code)



Obtém informações de clientes

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

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = "\"teste@teste.com.br\""; // string | Endereço de email do contato

try {
    $result = $apiInstance->clientsGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->clientsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **string**| Endereço de email do contato | [optional]

### Return type

[**\Swagger\Client\Model\Clients**](../Model/Clients.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **clientsPlansGet**
> \Swagger\Client\Model\Plans clientsPlansGet()



Obtém os planos disponíveis para os clientes

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

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->clientsPlansGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->clientsPlansGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Plans**](../Model/Plans.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **clientsPost**
> \Swagger\Client\Model\Clients clientsPost($code, $name, $tier, $active)

Apenas para clientes que tem autorização de criar clientes dentro de sua conta.

Acrescenta um cliente para utilização

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

$apiInstance = new Swagger\Client\Api\ClientsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = "\"email@myclient.com\""; // string | E-mail
$name = "\"Client's name\""; // string | Nome do cliente
$tier = 1; // int | Plano do cliente
$active = true; // bool | Se o cliente está ativo

try {
    $result = $apiInstance->clientsPost($code, $name, $tier, $active);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->clientsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **string**| E-mail |
 **name** | **string**| Nome do cliente |
 **tier** | **int**| Plano do cliente |
 **active** | **bool**| Se o cliente está ativo | [optional]

### Return type

[**\Swagger\Client\Model\Clients**](../Model/Clients.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

