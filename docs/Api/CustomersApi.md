# Swagger\Client\CustomersApi

All URIs are relative to *https://api.fulfilling.io/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**customerDelete**](CustomersApi.md#customerdelete) | **DELETE** /customer | 
[**customerGet**](CustomersApi.md#customerget) | **GET** /customer | 
[**customerPost**](CustomersApi.md#customerpost) | **POST** /customer | 
[**customersGet**](CustomersApi.md#customersget) | **GET** /customers | 

# **customerDelete**
> \Swagger\Client\Model\User customerDelete($customer_id)



Remove um determinado contato e destrói permanentemente as informações a ele associadas. (AINDA NÃO IMPLEMENTADO)

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

$apiInstance = new Swagger\Client\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_id = "customer_id_example"; // string | Identificação do contato

try {
    $result = $apiInstance->customerDelete($customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customerDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_id** | **string**| Identificação do contato |

### Return type

[**\Swagger\Client\Model\User**](../Model/User.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **customerGet**
> \Swagger\Client\Model\User customerGet($email, $customer_id)



Obtém informações de um dado contato

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

$apiInstance = new Swagger\Client\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email = "\"teste@teste.com.br\""; // string | Endereço de email do contato
$customer_id = "customer_id_example"; // string | Identificação do contato

try {
    $result = $apiInstance->customerGet($email, $customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customerGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **string**| Endereço de email do contato | [optional]
 **customer_id** | **string**| Identificação do contato | [optional]

### Return type

[**\Swagger\Client\Model\User**](../Model/User.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **customerPost**
> \Swagger\Client\Model\User customerPost($name, $email, $body, $telephone, $tags, $remove_tags, $custom)



Cria novo contato

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

$apiInstance = new Swagger\Client\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "\"Joaquim da Silva\""; // string | Nome do contato
$email = "\"teste@teste.com.br\""; // string | Endereço de email do contato
$body = new \Swagger\Client\Model\CustomerBody(); // \Swagger\Client\Model\CustomerBody | Campos personalizados
$telephone = "\"11 9999-9999\""; // string | Telefone do contato
$tags = array("[ \"id1\", \"id2\" ]"); // string[] | Id's das tags que serão atribuidas
$remove_tags = array("[ \"id1\", \"id2\" ]"); // string[] | Remove Id's das tags atribuidas
$custom = array(new \Swagger\Client\Model\string[]()); // string[][] | Informações dos campos customizados que serão enviados

try {
    $result = $apiInstance->customerPost($name, $email, $body, $telephone, $tags, $remove_tags, $custom);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customerPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Nome do contato |
 **email** | **string**| Endereço de email do contato |
 **body** | [**\Swagger\Client\Model\CustomerBody**](../Model/CustomerBody.md)| Campos personalizados | [optional]
 **telephone** | **string**| Telefone do contato | [optional]
 **tags** | [**string[]**](../Model/string.md)| Id&#x27;s das tags que serão atribuidas | [optional]
 **remove_tags** | [**string[]**](../Model/string.md)| Remove Id&#x27;s das tags atribuidas | [optional]
 **custom** | [**string[][]**](../Model/string[].md)| Informações dos campos customizados que serão enviados | [optional]

### Return type

[**\Swagger\Client\Model\User**](../Model/User.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **customersGet**
> \Swagger\Client\Model\Customers customersGet($tags)



Busca por contatos de acordo a certos critérios (não implementado)

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

$apiInstance = new Swagger\Client\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("[ \"5cbf91a1f7473d11f524ec85\", \"5cd48b32f7473d27de6b279f\" ]"); // string[] | id's de etiquetas

try {
    $result = $apiInstance->customersGet($tags);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->customersGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| id&#x27;s de etiquetas | [optional]

### Return type

[**\Swagger\Client\Model\Customers**](../Model/Customers.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

