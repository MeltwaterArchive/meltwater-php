# Swagger\Client\SchemasApi

All URIs are relative to *https://api.meltwater.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getEditorialStreamingJsonSchema**](SchemasApi.md#getEditorialStreamingJsonSchema) | **GET** /v2/schemas/editorial_streaming.json | Editorial Streaming JSON schema
[**getSocialStreamingJsonSchema**](SchemasApi.md#getSocialStreamingJsonSchema) | **GET** /v2/schemas/social_streaming.json | Social Streaming JSON schema


# **getEditorialStreamingJsonSchema**
> getEditorialStreamingJsonSchema($user_key)

Editorial Streaming JSON schema

Get the JSON schema describing the layout of Editorial Streaming documents.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\SchemasApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/).

try {
    $api_instance->getEditorialStreamingJsonSchema($user_key);
} catch (Exception $e) {
    echo 'Exception when calling SchemasApi->getEditorialStreamingJsonSchema: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/). |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSocialStreamingJsonSchema**
> getSocialStreamingJsonSchema($user_key)

Social Streaming JSON schema

Get the JSON schema describing the layout of Social Streaming documents.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\SchemasApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/).

try {
    $api_instance->getSocialStreamingJsonSchema($user_key);
} catch (Exception $e) {
    echo 'Exception when calling SchemasApi->getSocialStreamingJsonSchema: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/). |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

