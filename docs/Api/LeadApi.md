# Swagger\Client\LeadApi

All URIs are relative to *https://api.fulfilling.io/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**leadGet**](LeadApi.md#leadget) | **GET** /lead | 
[**leadPost**](LeadApi.md#leadpost) | **POST** /lead | 
[**leadResponsiblePost**](LeadApi.md#leadresponsiblepost) | **POST** /lead/responsible | 

# **leadGet**
> \Swagger\Client\Model\Lead leadGet($lead_id)



Obtém informações do lead

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

$apiInstance = new Swagger\Client\Api\LeadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$lead_id = "1234"; // string | Número interno

try {
    $result = $apiInstance->leadGet($lead_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeadApi->leadGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lead_id** | **string**| Número interno |

### Return type

[**\Swagger\Client\Model\Lead**](../Model/Lead.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **leadPost**
> \Swagger\Client\Model\Lead leadPost($id, $name, $telephone, $email, $body, $origin, $product_url, $product_id, $product_type, $product_subtype, $campaign, $utm_source, $utm_medium, $utm_campaign)



Insere um LEAD e obtém o \"Contact Score\"

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

$apiInstance = new Swagger\Client\Api\LeadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "53275"; // int | Identificação do Contato
$name = "\"Joaquim da Silva\""; // string | Nome do contato
$telephone = "\"551899999999\""; // string | Número de telefone (formato auto-detectado)
$email = "\"xxx@yahoo.com\""; // string | Endereço de e-mail do Contato
$body = new \Swagger\Client\Model\LeadBody(); // \Swagger\Client\Model\LeadBody | 
$origin = "\"landingpage\""; // string | Identificação do ponto de origem do contato
$product_url = "product_url_example"; // string | URL de página de Produto
$product_id = "product_id_example"; // string | Identificação de Produto
$product_type = "product_type_example"; // string | Categoria principal de produto ou tipo de transação
$product_subtype = "product_subtype_example"; // string | Sub-categoria ou sub-tipo de produto
$campaign = "campaign_example"; // string | Id da campanha vinculada
$utm_source = "utm_source_example"; // string | Origem de campanha
$utm_medium = "utm_medium_example"; // string | Meio de campanha
$utm_campaign = "utm_campaign_example"; // string | Nome de campanha

try {
    $result = $apiInstance->leadPost($id, $name, $telephone, $email, $body, $origin, $product_url, $product_id, $product_type, $product_subtype, $campaign, $utm_source, $utm_medium, $utm_campaign);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeadApi->leadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Identificação do Contato |
 **name** | **string**| Nome do contato |
 **telephone** | **string**| Número de telefone (formato auto-detectado) |
 **email** | **string**| Endereço de e-mail do Contato |
 **body** | [**\Swagger\Client\Model\LeadBody**](../Model/LeadBody.md)|  | [optional]
 **origin** | **string**| Identificação do ponto de origem do contato | [optional]
 **product_url** | **string**| URL de página de Produto | [optional]
 **product_id** | **string**| Identificação de Produto | [optional]
 **product_type** | **string**| Categoria principal de produto ou tipo de transação | [optional]
 **product_subtype** | **string**| Sub-categoria ou sub-tipo de produto | [optional]
 **campaign** | **string**| Id da campanha vinculada | [optional]
 **utm_source** | **string**| Origem de campanha | [optional]
 **utm_medium** | **string**| Meio de campanha | [optional]
 **utm_campaign** | **string**| Nome de campanha | [optional]

### Return type

[**\Swagger\Client\Model\Lead**](../Model/Lead.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **leadResponsiblePost**
> leadResponsiblePost($lead_id, $responsible_for_customer_service_name, $responsible_for_customer_service_email, $responsible_for_customer_service_telephone, $responsible_for_customer_service_avatar)



Atribui um atendente a um lead

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

$apiInstance = new Swagger\Client\Api\LeadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$lead_id = "\"5af1a78ef7473d1ac85f93d5\""; // string | Id do lead no FFID
$responsible_for_customer_service_name = "\"Mestre dos Magos\""; // string | Nome da pessoa responsável pelo lead
$responsible_for_customer_service_email = "\"mestre@ffid.com.br\""; // string | E-mail da pessoa responsável pelo lead
$responsible_for_customer_service_telephone = "\"(11) 99938-1234\""; // string | Telefone da pessoa responsável pelo lead
$responsible_for_customer_service_avatar = "\"http://www.meusite.com.br/minha-foto\""; // string | Foto da pessoa responsável pelo lead

try {
    $apiInstance->leadResponsiblePost($lead_id, $responsible_for_customer_service_name, $responsible_for_customer_service_email, $responsible_for_customer_service_telephone, $responsible_for_customer_service_avatar);
} catch (Exception $e) {
    echo 'Exception when calling LeadApi->leadResponsiblePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lead_id** | **string**| Id do lead no FFID |
 **responsible_for_customer_service_name** | **string**| Nome da pessoa responsável pelo lead |
 **responsible_for_customer_service_email** | **string**| E-mail da pessoa responsável pelo lead |
 **responsible_for_customer_service_telephone** | **string**| Telefone da pessoa responsável pelo lead |
 **responsible_for_customer_service_avatar** | **string**| Foto da pessoa responsável pelo lead | [optional]

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

