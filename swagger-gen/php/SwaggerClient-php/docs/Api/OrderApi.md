# Swagger\Client\OrderApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**orderCancel**](OrderApi.md#orderCancel) | **POST** /open-api/order/cancel | Get my active order list.
[**orderGetOrders**](OrderApi.md#orderGetOrders) | **GET** /open-api/order/list | Get my active order list.
[**orderNew**](OrderApi.md#orderNew) | **POST** /open-api/order/create | Place active order


# **orderCancel**
> object orderCancel($order_id, $symbol)

Get my active order list.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = "order_id_example"; // string | Order ID
$symbol = "symbol_example"; // string | Contract type.

try {
    $result = $apiInstance->orderCancel($order_id, $symbol);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderCancel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**| Order ID |
 **symbol** | **string**| Contract type. | [optional]

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **orderGetOrders**
> object orderGetOrders($order_id, $order_link_id, $symbol, $order, $page, $limit, $order_status)

Get my active order list.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = "order_id_example"; // string | Order ID
$order_link_id = "order_link_id_example"; // string | Customized order ID.
$symbol = "symbol_example"; // string | Contract type. Default BTCUSD
$order = "order_example"; // string | Sort orders by creation date
$page = 8.14; // float | Page. Default getting first page data
$limit = 8.14; // float | TLimit for data size per page, max size is 50. Default as showing 20 pieces of data per page
$order_status = "order_status_example"; // string | Query your orders for all statuses if 'order_status' is empty. If you want to query orders with specific statuses , you can pass the order_status split by

try {
    $result = $apiInstance->orderGetOrders($order_id, $order_link_id, $symbol, $order, $page, $limit, $order_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderGetOrders: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**| Order ID | [optional]
 **order_link_id** | **string**| Customized order ID. | [optional]
 **symbol** | **string**| Contract type. Default BTCUSD | [optional]
 **order** | **string**| Sort orders by creation date | [optional]
 **page** | **float**| Page. Default getting first page data | [optional]
 **limit** | **float**| TLimit for data size per page, max size is 50. Default as showing 20 pieces of data per page | [optional]
 **order_status** | **string**| Query your orders for all statuses if &#39;order_status&#39; is empty. If you want to query orders with specific statuses , you can pass the order_status split by | [optional]

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **orderNew**
> object orderNew($side, $symbol, $order_type, $qty, $price, $time_in_force, $take_profit, $stop_loss, $reduce_only, $close_on_trigger, $order_link_id)

Place active order

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$side = "side_example"; // string | Side
$symbol = "symbol_example"; // string | Contract type.
$order_type = "order_type_example"; // string | Active order type
$qty = 8.14; // float | 
$price = 1.2; // double | Order price.
$time_in_force = "time_in_force_example"; // string | Time in force
$take_profit = 1.2; // double | take profit price
$stop_loss = 1.2; // double | stop loss price
$reduce_only = true; // bool | reduce only
$close_on_trigger = true; // bool | close on trigger
$order_link_id = "order_link_id_example"; // string | TCustomized order ID, maximum length at 36 characters, and order ID under the same agency has to be unique.

try {
    $result = $apiInstance->orderNew($side, $symbol, $order_type, $qty, $price, $time_in_force, $take_profit, $stop_loss, $reduce_only, $close_on_trigger, $order_link_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderNew: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **side** | **string**| Side |
 **symbol** | **string**| Contract type. |
 **order_type** | **string**| Active order type |
 **qty** | **float**|  |
 **price** | **double**| Order price. |
 **time_in_force** | **string**| Time in force |
 **take_profit** | **double**| take profit price | [optional]
 **stop_loss** | **double**| stop loss price | [optional]
 **reduce_only** | **bool**| reduce only | [optional]
 **close_on_trigger** | **bool**| close on trigger | [optional]
 **order_link_id** | **string**| TCustomized order ID, maximum length at 36 characters, and order ID under the same agency has to be unique. | [optional]

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)
