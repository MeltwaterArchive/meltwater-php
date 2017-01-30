# Swagger\Client\HooksApi

All URIs are relative to *https://api.meltwater.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteV1HooksId**](HooksApi.md#deleteV1HooksId) | **DELETE** /v1/hooks/{id} | Delete an existing hook.
[**getV1Hooks**](HooksApi.md#getV1Hooks) | **GET** /v1/hooks | List all hooks.
[**postV1Hooks**](HooksApi.md#postV1Hooks) | **POST** /v1/hooks | Creates a hook for one of your predefined searches.


# **deleteV1HooksId**
> deleteV1HooksId($user_key, $authorization, $id)

Delete an existing hook.

Delete an existing hook.  Removes the hook and stops sending any search results to the target_url.    Requires an OAuth access token.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\HooksApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.io](https://developer.meltwater.io/admin/applications/).
$authorization = "authorization_example"; // string | `Oauth Access Token`    OAuth access token (RFC 6749). Must contain the access token type `Bearer`  followed by an OAuth access token.    #### Example:        Bearer KKwmfHwxsEoeMDTMAfxOpO...
$id = "id_example"; // string | Hook ID received from creating a hook

try {
    $api_instance->deleteV1HooksId($user_key, $authorization, $id);
} catch (Exception $e) {
    echo 'Exception when calling HooksApi->deleteV1HooksId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.io](https://developer.meltwater.io/admin/applications/). |
 **authorization** | **string**| &#x60;Oauth Access Token&#x60;    OAuth access token (RFC 6749). Must contain the access token type &#x60;Bearer&#x60;  followed by an OAuth access token.    #### Example:        Bearer KKwmfHwxsEoeMDTMAfxOpO... |
 **id** | **string**| Hook ID received from creating a hook |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getV1Hooks**
> \Swagger\Client\Model\HooksCollection getV1Hooks($user_key, $authorization)

List all hooks.

List all hooks.     Delivers all previously generated hooks.    Requires an OAuth access token.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\HooksApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.io](https://developer.meltwater.io/admin/applications/).
$authorization = "authorization_example"; // string | `Oauth Access Token`    OAuth access token (RFC 6749). Must contain the access token type `Bearer`  followed by an OAuth access token.    #### Example:        Bearer KKwmfHwxsEoeMDTMAfxOpO...

try {
    $result = $api_instance->getV1Hooks($user_key, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HooksApi->getV1Hooks: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.io](https://developer.meltwater.io/admin/applications/). |
 **authorization** | **string**| &#x60;Oauth Access Token&#x60;    OAuth access token (RFC 6749). Must contain the access token type &#x60;Bearer&#x60;  followed by an OAuth access token.    #### Example:        Bearer KKwmfHwxsEoeMDTMAfxOpO... |

### Return type

[**\Swagger\Client\Model\HooksCollection**](../Model/HooksCollection.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postV1Hooks**
> \Swagger\Client\Model\Hook postV1Hooks($user_key, $authorization, $v1_hooks)

Creates a hook for one of your predefined searches.

Creates a hook for one of your predefined searches.  Delivers search results for the query referenced by thesearch_id to the target_url via HTTP POST. Note that a hook id will be returned on successful creation, this id is needed to delete the hook.     Requires an OAuth access token.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\HooksApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.io](https://developer.meltwater.io/admin/applications/).
$authorization = "authorization_example"; // string | `Oauth Access Token`    OAuth access token (RFC 6749). Must contain the access token type `Bearer`  followed by an OAuth access token.    #### Example:        Bearer KKwmfHwxsEoeMDTMAfxOpO...
$v1_hooks = new \Swagger\Client\Model\PostV1Hooks(); // \Swagger\Client\Model\PostV1Hooks | 

try {
    $result = $api_instance->postV1Hooks($user_key, $authorization, $v1_hooks);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HooksApi->postV1Hooks: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.io](https://developer.meltwater.io/admin/applications/). |
 **authorization** | **string**| &#x60;Oauth Access Token&#x60;    OAuth access token (RFC 6749). Must contain the access token type &#x60;Bearer&#x60;  followed by an OAuth access token.    #### Example:        Bearer KKwmfHwxsEoeMDTMAfxOpO... |
 **v1_hooks** | [**\Swagger\Client\Model\PostV1Hooks**](../Model/\Swagger\Client\Model\PostV1Hooks.md)|  |

### Return type

[**\Swagger\Client\Model\Hook**](../Model/Hook.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

