# Swagger\Client\ListsApi

All URIs are relative to *https://api.fulfilling.io/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listsCustomerDelete**](ListsApi.md#listscustomerdelete) | **DELETE** /lists/customer | 
[**listsCustomerPost**](ListsApi.md#listscustomerpost) | **POST** /lists/customer | 

# **listsCustomerDelete**
> listsCustomerDelete($list_id, $telephone, $email)



Remove contato de uma lista

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

$apiInstance = new Swagger\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$list_id = "\"5b17ff2ef7473d4e6d51dc73\""; // string | Identificação da Lista
$telephone = "\"11 9999-9999\""; // string | Telefone do contato
$email = "\"teste@teste.com.br\""; // string | Endereço de email do contato

try {
    $apiInstance->listsCustomerDelete($list_id, $telephone, $email);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->listsCustomerDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **list_id** | **string**| Identificação da Lista | [optional]
 **telephone** | **string**| Telefone do contato | [optional]
 **email** | **string**| Endereço de email do contato | [optional]

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listsCustomerPost**
> listsCustomerPost($list_id, $telephone, $email)



Acrescenta contato a uma lista

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

$apiInstance = new Swagger\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$list_id = "\"5b17ff2ef7473d4e6d51dc73\""; // string | Identificação da Lista
$telephone = "\"11 9999-9999\""; // string | Telefone do contato
$email = "\"teste@teste.com.br\""; // string | Endereço de email do contato

try {
    $apiInstance->listsCustomerPost($list_id, $telephone, $email);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->listsCustomerPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **list_id** | **string**| Identificação da Lista |
 **telephone** | **string**| Telefone do contato | [optional]
 **email** | **string**| Endereço de email do contato | [optional]

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

