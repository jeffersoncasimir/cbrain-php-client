# Swagger\Client\ToolConfigsApi

All URIs are relative to *http://localhost:3000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**toolConfigsGet**](ToolConfigsApi.md#toolConfigsGet) | **GET** /tool_configs | Get a list of tool versions installed.
[**toolConfigsIdGet**](ToolConfigsApi.md#toolConfigsIdGet) | **GET** /tool_configs/{id} | Get information about a particular tool configuration


# **toolConfigsGet**
> \Swagger\Client\Model\ToolConfig[] toolConfigsGet($page, $per_page)

Get a list of tool versions installed.

This method returns a list of tool config objects.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ToolConfigsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int | Page number when paginating. See also the per_page parameter
$per_page = 56; // int | Size of each page when paginating. See also the page parameter

try {
    $result = $apiInstance->toolConfigsGet($page, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ToolConfigsApi->toolConfigsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| Page number when paginating. See also the per_page parameter | [optional]
 **per_page** | **int**| Size of each page when paginating. See also the page parameter | [optional]

### Return type

[**\Swagger\Client\Model\ToolConfig[]**](../Model/ToolConfig.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **toolConfigsIdGet**
> \Swagger\Client\Model\ToolConfig toolConfigsIdGet($id)

Get information about a particular tool configuration

Returns the information about how a particular configuration of a tool on an execution server.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: BrainPortalSession
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('cbrain_api_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('cbrain_api_token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ToolConfigsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | the ID of the configuration

try {
    $result = $apiInstance->toolConfigsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ToolConfigsApi->toolConfigsIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| the ID of the configuration |

### Return type

[**\Swagger\Client\Model\ToolConfig**](../Model/ToolConfig.md)

### Authorization

[BrainPortalSession](../../README.md#BrainPortalSession)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

