# Chat

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Identificação da conversa | [optional] 
**client_id** | **string** | Identificação do Cliente FFID | [optional] 
**customer_id** | **string** |  | [optional] 
**account_manager** | **string** | Usuário a quem a Conversa está atribuída | [optional] 
**channel** | **string** |  | [optional] 
**pending_to_send** | **int** | Número de mensagens com envio agendado pendente | [optional] 
**pending_to_read** | **int** | Número de mensagens enviadas e ainda não lidas pelo Consumidor | [optional] 
**interactions** | [**\Swagger\Client\Model\Interaction[]**](Interaction.md) | Interações | [optional] 
**customer** | [**\Swagger\Client\Model\Customer**](Customer.md) |  | [optional] 
**device** | [**\Swagger\Client\Model\Device**](Device.md) |  | [optional] 
**status** | **string** |  | [optional] 
**reasons_to_close** | **string[]** | Lista de Motivos para encerramento da conversa | [optional] 
**tags** | **string[]** | Lista de Etiquetas atribuídas à Conversa | [optional] 
**active** | **int** |  | [optional] 
**last_message** | **string** | Última mensagem recebida do Consumidor | [optional] 
**created_at** | **string** | Data de criação da Conversa | [optional] 
**updated_at** | **string** | Data de último envio ou recebimento de mensagem | [optional] 
**messages** | [**\Swagger\Client\Model\Message[]**](Message.md) |  | [optional] 
**total_messages** | **int** | Total de mensagens nesta Conversa | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

