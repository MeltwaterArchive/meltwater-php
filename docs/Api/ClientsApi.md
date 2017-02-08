# Swagger\Client\ClientsApi

All URIs are relative to *https://api.meltwater.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createClientCredentials**](ClientsApi.md#createClientCredentials) | **POST** /v1/clients | Register new client
[**deleteClientCredentials**](ClientsApi.md#deleteClientCredentials) | **DELETE** /v1/clients/{client_id} | Delete client.


# **createClientCredentials**
> \Swagger\Client\Model\ClientCredentials createClientCredentials($user_key, $authorization)

Register new client

Register new client     Creates a new pair of client credentials (`client_id`/`client_secret` pair).  Requires your Meltwater credentials (`email`:`password`) to authenticate.   #### Appendix    The Base64-encoded `email`:`password` string can be generated in a terminal  with following command:        $ echo -n \"your_email@your_domain.com:your_secret_password\" | base64    <i>You will need `base64` installed.</i>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\ClientsApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/).
$authorization = "authorization_example"; // string | `email`:`password`    Basic Auth (RFC2617) credentials. Must contain the realm `Basic` followed by a  Base64-encoded `email`:`password` pair using your Meltwater credentials.    #### Example:        Basic bXlfZW1haWxAZXhhbXJzZWNyZXQ=

try {
    $result = $api_instance->createClientCredentials($user_key, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->createClientCredentials: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/). |
 **authorization** | **string**| &#x60;email&#x60;:&#x60;password&#x60;    Basic Auth (RFC2617) credentials. Must contain the realm &#x60;Basic&#x60; followed by a  Base64-encoded &#x60;email&#x60;:&#x60;password&#x60; pair using your Meltwater credentials.    #### Example:        Basic bXlfZW1haWxAZXhhbXJzZWNyZXQ&#x3D; |

### Return type

[**\Swagger\Client\Model\ClientCredentials**](../Model/ClientCredentials.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteClientCredentials**
> deleteClientCredentials($user_key, $authorization, $client_id)

Delete client.

Delete client.    Deletes your current client credentials consisting of  client_id and client_secret. After calling this resource, you will not be able  to use the Meltwater API unless you create a new set of client credentials!  Requires your Meltwater credentials (`email`:`password`) to authenticate.   #### Appendix    The Base64-encoded `email`:`password` string can be generated in a terminal  with following command:        $ echo -n \"your_email@your_domain.com:your_secret_password\" | base64    <i>You will need `base64` installed.</i>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\ClientsApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/).
$authorization = "authorization_example"; // string | `email`:`password`    Basic Auth (RFC2617) credentials. Must contain the realm `Basic` followed by a  Base64-encoded `email`:`password` pair using your Meltwater credentials.    #### Example:        Basic bXlfZW1haWxAZXhhbXJzZWNyZXQ=
$client_id = "client_id_example"; // string | Client ID

try {
    $api_instance->deleteClientCredentials($user_key, $authorization, $client_id);
} catch (Exception $e) {
    echo 'Exception when calling ClientsApi->deleteClientCredentials: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/). |
 **authorization** | **string**| &#x60;email&#x60;:&#x60;password&#x60;    Basic Auth (RFC2617) credentials. Must contain the realm &#x60;Basic&#x60; followed by a  Base64-encoded &#x60;email&#x60;:&#x60;password&#x60; pair using your Meltwater credentials.    #### Example:        Basic bXlfZW1haWxAZXhhbXJzZWNyZXQ&#x3D; |
 **client_id** | **string**| Client ID |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

