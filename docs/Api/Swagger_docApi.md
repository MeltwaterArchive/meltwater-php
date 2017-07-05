# Swagger\Client\Swagger_docApi

All URIs are relative to *https://api.meltwater.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCompleteSwaggerSpec**](Swagger_docApi.md#getCompleteSwaggerSpec) | **GET** /v2/swagger_doc | Meltwater API Swagger Spec


# **getCompleteSwaggerSpec**
> getCompleteSwaggerSpec($user_key)

Meltwater API Swagger Spec

Get the complete Swagger Spec that describes all Meltwater API endpoints.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\Swagger_docApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/).

try {
    $api_instance->getCompleteSwaggerSpec($user_key);
} catch (Exception $e) {
    echo 'Exception when calling Swagger_docApi->getCompleteSwaggerSpec: ', $e->getMessage(), PHP_EOL;
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

