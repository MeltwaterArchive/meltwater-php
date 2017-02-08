# Swagger\Client\OauthApi

All URIs are relative to *https://api.meltwater.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createToken**](OauthApi.md#createToken) | **POST** /oauth2/token | Create an access token


# **createToken**
> \Swagger\Client\Model\OAuth2Token createToken($user_key, $authorization, $grant_type, $scope)

Create an access token

Create an OAuth2 access token based on the provided `client_id` and `client_secret`

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\OauthApi();
$user_key = "user_key_example"; // string | The `user_key` from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/).
$authorization = "authorization_example"; // string | `client_id:client_secret`  Basic Auth (RFC2617) credentials. Must contain the realm `Basic` followed by a Base64-encoded `client_id`:`client_secret` pair.   #### Example:      Basic aAlfbb1haWxDSXhhDXxxZWKJAyZXQ=
$grant_type = "grant_type_example"; // string | OAuth2 grant type, use `client_credentials`
$scope = "scope_example"; // string | OAuth2 scope, use `search`

try {
    $result = $api_instance->createToken($user_key, $authorization, $grant_type, $scope);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OauthApi->createToken: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_key** | **string**| The &#x60;user_key&#x60; from [developer.meltwater.com](https://developer.meltwater.com/admin/applications/). |
 **authorization** | **string**| &#x60;client_id:client_secret&#x60;  Basic Auth (RFC2617) credentials. Must contain the realm &#x60;Basic&#x60; followed by a Base64-encoded &#x60;client_id&#x60;:&#x60;client_secret&#x60; pair.   #### Example:      Basic aAlfbb1haWxDSXhhDXxxZWKJAyZXQ&#x3D; |
 **grant_type** | **string**| OAuth2 grant type, use &#x60;client_credentials&#x60; |
 **scope** | **string**| OAuth2 scope, use &#x60;search&#x60; |

### Return type

[**\Swagger\Client\Model\OAuth2Token**](../Model/OAuth2Token.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

