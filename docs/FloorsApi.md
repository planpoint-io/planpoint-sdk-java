# FloorsApi

All URIs are relative to *https://app.planpoint.io*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createFloor**](FloorsApi.md#createFloor) | **POST** /api/floors | Create a floor |
| [**createFloorWithHttpInfo**](FloorsApi.md#createFloorWithHttpInfo) | **POST** /api/floors | Create a floor |
| [**getFloor**](FloorsApi.md#getFloor) | **GET** /api/floors/{id} | Get a floor by ID |
| [**getFloorWithHttpInfo**](FloorsApi.md#getFloorWithHttpInfo) | **GET** /api/floors/{id} | Get a floor by ID |
| [**getFloors**](FloorsApi.md#getFloors) | **GET** /api/floors | Get floors for a project |
| [**getFloorsWithHttpInfo**](FloorsApi.md#getFloorsWithHttpInfo) | **GET** /api/floors | Get floors for a project |
| [**updateFloor**](FloorsApi.md#updateFloor) | **PATCH** /api/floors/{id} | Update a floor |
| [**updateFloorWithHttpInfo**](FloorsApi.md#updateFloorWithHttpInfo) | **PATCH** /api/floors/{id} | Update a floor |



## createFloor

> FloorFull createFloor(createFloorBody)

Create a floor

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.FloorsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        FloorsApi apiInstance = new FloorsApi(defaultClient);
        CreateFloorBody createFloorBody = new CreateFloorBody(); // CreateFloorBody | 
        try {
            FloorFull result = apiInstance.createFloor(createFloorBody);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling FloorsApi#createFloor");
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
| **createFloorBody** | [**CreateFloorBody**](CreateFloorBody.md)|  | |

### Return type

[**FloorFull**](FloorFull.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created floor |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## createFloorWithHttpInfo

> ApiResponse<FloorFull> createFloorWithHttpInfo(createFloorBody)

Create a floor

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.FloorsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        FloorsApi apiInstance = new FloorsApi(defaultClient);
        CreateFloorBody createFloorBody = new CreateFloorBody(); // CreateFloorBody | 
        try {
            ApiResponse<FloorFull> response = apiInstance.createFloorWithHttpInfo(createFloorBody);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling FloorsApi#createFloor");
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
| **createFloorBody** | [**CreateFloorBody**](CreateFloorBody.md)|  | |

### Return type

ApiResponse<[**FloorFull**](FloorFull.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created floor |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## getFloor

> FloorFull getFloor(id)

Get a floor by ID

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.FloorsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        FloorsApi apiInstance = new FloorsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            FloorFull result = apiInstance.getFloor(id);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling FloorsApi#getFloor");
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

[**FloorFull**](FloorFull.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Floor |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## getFloorWithHttpInfo

> ApiResponse<FloorFull> getFloorWithHttpInfo(id)

Get a floor by ID

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.FloorsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        FloorsApi apiInstance = new FloorsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            ApiResponse<FloorFull> response = apiInstance.getFloorWithHttpInfo(id);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling FloorsApi#getFloor");
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

ApiResponse<[**FloorFull**](FloorFull.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Floor |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## getFloors

> List<FloorFull> getFloors(pid)

Get floors for a project

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.FloorsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        FloorsApi apiInstance = new FloorsApi(defaultClient);
        String pid = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            List<FloorFull> result = apiInstance.getFloors(pid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling FloorsApi#getFloors");
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

[**List&lt;FloorFull&gt;**](FloorFull.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Floors list |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## getFloorsWithHttpInfo

> ApiResponse<List<FloorFull>> getFloorsWithHttpInfo(pid)

Get floors for a project

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.FloorsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        FloorsApi apiInstance = new FloorsApi(defaultClient);
        String pid = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            ApiResponse<List<FloorFull>> response = apiInstance.getFloorsWithHttpInfo(pid);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling FloorsApi#getFloors");
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

ApiResponse<[**List&lt;FloorFull&gt;**](FloorFull.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Floors list |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## updateFloor

> FloorFull updateFloor(id, requestBody)

Update a floor

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.FloorsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        FloorsApi apiInstance = new FloorsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        Map<String, Object> requestBody = null; // Map<String, Object> | 
        try {
            FloorFull result = apiInstance.updateFloor(id, requestBody);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling FloorsApi#updateFloor");
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

[**FloorFull**](FloorFull.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated floor |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## updateFloorWithHttpInfo

> ApiResponse<FloorFull> updateFloorWithHttpInfo(id, requestBody)

Update a floor

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.FloorsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        FloorsApi apiInstance = new FloorsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        Map<String, Object> requestBody = null; // Map<String, Object> | 
        try {
            ApiResponse<FloorFull> response = apiInstance.updateFloorWithHttpInfo(id, requestBody);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling FloorsApi#updateFloor");
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

ApiResponse<[**FloorFull**](FloorFull.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated floor |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

