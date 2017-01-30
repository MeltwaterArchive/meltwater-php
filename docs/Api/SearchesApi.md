# Swagger\Client\SearchesApi

All URIs are relative to *https://api.meltwater.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getV1Searches**](SearchesApi.md#getV1Searches) | **GET** /v1/searches | List your saved searches.


# **getV1Searches**
> \Swagger\Client\Model\SearchesCollection getV1Searches($user_key, $authorization)

List your saved searches.

List your saved searches.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\SearchesApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.io](https://developer.meltwater.io/admin/applications/).
$authorization = "authorization_example"; // string | `Oauth Access Token`    OAuth access token (RFC 6749). Must contain the access token type `Bearer`  followed by an OAuth access token.    #### Example:        Bearer KKwmfHwxsEoeMDTMAfxOpO...

try {
    $result = $api_instance->getV1Searches($user_key, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchesApi->getV1Searches: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.io](https://developer.meltwater.io/admin/applications/). |
 **authorization** | **string**| &#x60;Oauth Access Token&#x60;    OAuth access token (RFC 6749). Must contain the access token type &#x60;Bearer&#x60;  followed by an OAuth access token.    #### Example:        Bearer KKwmfHwxsEoeMDTMAfxOpO... |

### Return type

[**\Swagger\Client\Model\SearchesCollection**](../Model/SearchesCollection.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

