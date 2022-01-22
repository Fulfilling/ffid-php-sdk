# Swagger\Client\ChatApi

All URIs are relative to *https://api.fulfilling.io/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatChatsGet**](ChatApi.md#chatchatsget) | **GET** /chat/chats | 
[**chatMessagePost**](ChatApi.md#chatmessagepost) | **POST** /chat/message | 
[**chatMessagesGet**](ChatApi.md#chatmessagesget) | **GET** /chat/messages | 
[**emailPost**](ChatApi.md#emailpost) | **POST** /email | 
[**smsPost**](ChatApi.md#smspost) | **POST** /sms | 

# **chatChatsGet**
> \Swagger\Client\Model\Chats chatChatsGet($page, $id, $q, $user_id, $view, $tag)



Retorna conversas segundo diversos critérios de busca

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

$apiInstance = new Swagger\Client\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | Página de resultados
$id = "id_example"; // string | Identificação da Conversa
$q = "q_example"; // string | Query - texto para busca genérica
$user_id = "user_id_example"; // string | Usuário a quem a conversa está atribuída
$view = "view_example"; // string | Escopo de visualização ('all', 'mine', 'unassigned')
$tag = "tag_example"; // string | Identificação da Etiqueta

try {
    $result = $apiInstance->chatChatsGet($page, $id, $q, $user_id, $view, $tag);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->chatChatsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| Página de resultados | [optional]
 **id** | **string**| Identificação da Conversa | [optional]
 **q** | **string**| Query - texto para busca genérica | [optional]
 **user_id** | **string**| Usuário a quem a conversa está atribuída | [optional]
 **view** | **string**| Escopo de visualização (&#x27;all&#x27;, &#x27;mine&#x27;, &#x27;unassigned&#x27;) | [optional]
 **tag** | **string**| Identificação da Etiqueta | [optional]

### Return type

[**\Swagger\Client\Model\Chats**](../Model/Chats.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **chatMessagePost**
> \Swagger\Client\Model\Chat chatMessagePost($telephone, $date, $message, $template_id, $media)



Envia nova mensagem em uma conversa

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

$apiInstance = new Swagger\Client\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$telephone = "\"(11) 99938-6810\""; // string | Número de telefone (formato auto-detectado)
$date = "\"2018-05-24 08:20\""; // string | Data agendada para envio da mensagem
$message = "\"Bom dia!\""; // string | Conteúdo de texto da mensagem
$template_id = "\"5af1a78ef7473d1ac85f93d5\""; // string | Identificação do modelo de mensagem
$media = "media_example"; // string | URL de arquivo a anexar

try {
    $result = $apiInstance->chatMessagePost($telephone, $date, $message, $template_id, $media);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->chatMessagePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **telephone** | **string**| Número de telefone (formato auto-detectado) |
 **date** | **string**| Data agendada para envio da mensagem | [optional]
 **message** | **string**| Conteúdo de texto da mensagem | [optional]
 **template_id** | **string**| Identificação do modelo de mensagem | [optional]
 **media** | **string**| URL de arquivo a anexar | [optional]

### Return type

[**\Swagger\Client\Model\Chat**](../Model/Chat.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **chatMessagesGet**
> \Swagger\Client\Model\Chat chatMessagesGet($telephone)



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

$apiInstance = new Swagger\Client\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$telephone = "\"(11) 99938-6810\""; // string | Número de telefone (formato auto-detectado)

try {
    $result = $apiInstance->chatMessagesGet($telephone);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->chatMessagesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **telephone** | **string**| Número de telefone (formato auto-detectado) |

### Return type

[**\Swagger\Client\Model\Chat**](../Model/Chat.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailPost**
> \Swagger\Client\Model\Chat emailPost($email, $message_title, $message, $sender_id, $template_id)



Envia nova mensagem por SMS em uma conversa

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

$apiInstance = new Swagger\Client\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email = "\"raphael@ffid.com.br\""; // string | email
$message_title = "\"Titulo\""; // string | Titulo do email
$message = "\"<html><body>Bom dia!</body></html>\""; // string | Conteúdo de texto da mensagem, deve ser transformado em BASE64
$sender_id = "\"5af1a78ef7473d1ac85f93d5\""; // string | Identificação do email que vai enviar a mensagem
$template_id = "\"5af1a78ef7473d1ac85f93d5\""; // string | Identificação do modelo de mensagem

try {
    $result = $apiInstance->emailPost($email, $message_title, $message, $sender_id, $template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->emailPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **string**| email |
 **message_title** | **string**| Titulo do email | [optional]
 **message** | **string**| Conteúdo de texto da mensagem, deve ser transformado em BASE64 | [optional]
 **sender_id** | **string**| Identificação do email que vai enviar a mensagem | [optional]
 **template_id** | **string**| Identificação do modelo de mensagem | [optional]

### Return type

[**\Swagger\Client\Model\Chat**](../Model/Chat.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsPost**
> \Swagger\Client\Model\Chat smsPost($telephone, $message, $template_id)



Envia nova mensagem por SMS em uma conversa

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

$apiInstance = new Swagger\Client\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$telephone = "\"(11) 99938-6810\""; // string | Número de telefone (formato auto-detectado)
$message = "\"Bom dia!\""; // string | Conteúdo de texto da mensagem
$template_id = "\"5af1a78ef7473d1ac85f93d5\""; // string | Identificação do modelo de mensagem

try {
    $result = $apiInstance->smsPost($telephone, $message, $template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->smsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **telephone** | **string**| Número de telefone (formato auto-detectado) |
 **message** | **string**| Conteúdo de texto da mensagem | [optional]
 **template_id** | **string**| Identificação do modelo de mensagem | [optional]

### Return type

[**\Swagger\Client\Model\Chat**](../Model/Chat.md)

### Authorization

[api_key](../../README.md#api_key), [api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

