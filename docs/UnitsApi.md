# UnitsApi

All URIs are relative to *https://app.planpoint.io*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**batchUpdateUnits**](UnitsApi.md#batchUpdateUnits) | **PATCH** /api/units | Batch update units |
| [**batchUpdateUnitsWithHttpInfo**](UnitsApi.md#batchUpdateUnitsWithHttpInfo) | **PATCH** /api/units | Batch update units |
| [**createUnit**](UnitsApi.md#createUnit) | **POST** /api/units | Create a unit |
| [**createUnitWithHttpInfo**](UnitsApi.md#createUnitWithHttpInfo) | **POST** /api/units | Create a unit |
| [**deleteUnit**](UnitsApi.md#deleteUnit) | **DELETE** /api/units/{id} | Delete a unit |
| [**deleteUnitWithHttpInfo**](UnitsApi.md#deleteUnitWithHttpInfo) | **DELETE** /api/units/{id} | Delete a unit |
| [**getUnit**](UnitsApi.md#getUnit) | **GET** /api/units/{id} | Get a unit by ID |
| [**getUnitWithHttpInfo**](UnitsApi.md#getUnitWithHttpInfo) | **GET** /api/units/{id} | Get a unit by ID |
| [**getUnits**](UnitsApi.md#getUnits) | **GET** /api/units | Get units for a project |
| [**getUnitsWithHttpInfo**](UnitsApi.md#getUnitsWithHttpInfo) | **GET** /api/units | Get units for a project |
| [**updateUnit**](UnitsApi.md#updateUnit) | **PATCH** /api/units/{id} | Update a unit |
| [**updateUnitWithHttpInfo**](UnitsApi.md#updateUnitWithHttpInfo) | **PATCH** /api/units/{id} | Update a unit |



## batchUpdateUnits

> List<UnitFull> batchUpdateUnits(batchUpdateUnitsBody)

Batch update units

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        BatchUpdateUnitsBody batchUpdateUnitsBody = new BatchUpdateUnitsBody(); // BatchUpdateUnitsBody | 
        try {
            List<UnitFull> result = apiInstance.batchUpdateUnits(batchUpdateUnitsBody);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#batchUpdateUnits");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **batchUpdateUnitsBody** | [**BatchUpdateUnitsBody**](BatchUpdateUnitsBody.md)|  | |

### Return type

[**List&lt;UnitFull&gt;**](UnitFull.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Updated units |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## batchUpdateUnitsWithHttpInfo

> ApiResponse<List<UnitFull>> batchUpdateUnitsWithHttpInfo(batchUpdateUnitsBody)

Batch update units

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        BatchUpdateUnitsBody batchUpdateUnitsBody = new BatchUpdateUnitsBody(); // BatchUpdateUnitsBody | 
        try {
            ApiResponse<List<UnitFull>> response = apiInstance.batchUpdateUnitsWithHttpInfo(batchUpdateUnitsBody);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#batchUpdateUnits");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **batchUpdateUnitsBody** | [**BatchUpdateUnitsBody**](BatchUpdateUnitsBody.md)|  | |

### Return type

ApiResponse<[**List&lt;UnitFull&gt;**](UnitFull.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Updated units |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## createUnit

> UnitFull createUnit(createUnitBody)

Create a unit

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        CreateUnitBody createUnitBody = new CreateUnitBody(); // CreateUnitBody | 
        try {
            UnitFull result = apiInstance.createUnit(createUnitBody);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#createUnit");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createUnitBody** | [**CreateUnitBody**](CreateUnitBody.md)|  | |

### Return type

[**UnitFull**](UnitFull.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created unit |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## createUnitWithHttpInfo

> ApiResponse<UnitFull> createUnitWithHttpInfo(createUnitBody)

Create a unit

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        CreateUnitBody createUnitBody = new CreateUnitBody(); // CreateUnitBody | 
        try {
            ApiResponse<UnitFull> response = apiInstance.createUnitWithHttpInfo(createUnitBody);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#createUnit");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createUnitBody** | [**CreateUnitBody**](CreateUnitBody.md)|  | |

### Return type

ApiResponse<[**UnitFull**](UnitFull.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created unit |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## deleteUnit

> ErrorResponse deleteUnit(id)

Delete a unit

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            ErrorResponse result = apiInstance.deleteUnit(id);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#deleteUnit");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |

### Return type

[**ErrorResponse**](ErrorResponse.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Unit deleted |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## deleteUnitWithHttpInfo

> ApiResponse<ErrorResponse> deleteUnitWithHttpInfo(id)

Delete a unit

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            ApiResponse<ErrorResponse> response = apiInstance.deleteUnitWithHttpInfo(id);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#deleteUnit");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |

### Return type

ApiResponse<[**ErrorResponse**](ErrorResponse.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Unit deleted |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## getUnit

> UnitFull getUnit(id)

Get a unit by ID

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            UnitFull result = apiInstance.getUnit(id);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#getUnit");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |

### Return type

[**UnitFull**](UnitFull.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Unit |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## getUnitWithHttpInfo

> ApiResponse<UnitFull> getUnitWithHttpInfo(id)

Get a unit by ID

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            ApiResponse<UnitFull> response = apiInstance.getUnitWithHttpInfo(id);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#getUnit");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |

### Return type

ApiResponse<[**UnitFull**](UnitFull.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Unit |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## getUnits

> UnitsListResponse getUnits(pid)

Get units for a project

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        String pid = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            UnitsListResponse result = apiInstance.getUnits(pid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#getUnits");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **pid** | **String**|  | |

### Return type

[**UnitsListResponse**](UnitsListResponse.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Units list |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## getUnitsWithHttpInfo

> ApiResponse<UnitsListResponse> getUnitsWithHttpInfo(pid)

Get units for a project

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        String pid = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            ApiResponse<UnitsListResponse> response = apiInstance.getUnitsWithHttpInfo(pid);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#getUnits");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **pid** | **String**|  | |

### Return type

ApiResponse<[**UnitsListResponse**](UnitsListResponse.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Units list |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## updateUnit

> UnitFull updateUnit(id, requestBody)

Update a unit

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        Map<String, Object> requestBody = null; // Map<String, Object> | 
        try {
            UnitFull result = apiInstance.updateUnit(id, requestBody);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#updateUnit");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |
| **requestBody** | [**Map&lt;String, Object&gt;**](Object.md)|  | |

### Return type

[**UnitFull**](UnitFull.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated unit |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## updateUnitWithHttpInfo

> ApiResponse<UnitFull> updateUnitWithHttpInfo(id, requestBody)

Update a unit

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.UnitsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        UnitsApi apiInstance = new UnitsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        Map<String, Object> requestBody = null; // Map<String, Object> | 
        try {
            ApiResponse<UnitFull> response = apiInstance.updateUnitWithHttpInfo(id, requestBody);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling UnitsApi#updateUnit");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |
| **requestBody** | [**Map&lt;String, Object&gt;**](Object.md)|  | |

### Return type

ApiResponse<[**UnitFull**](UnitFull.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated unit |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

