# GroupsApi

All URIs are relative to *https://app.planpoint.io*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createGroup**](GroupsApi.md#createGroup) | **POST** /api/groups | Create a group |
| [**createGroupWithHttpInfo**](GroupsApi.md#createGroupWithHttpInfo) | **POST** /api/groups | Create a group |
| [**getGroup**](GroupsApi.md#getGroup) | **GET** /api/groups/{id} | Get a group by ID |
| [**getGroupWithHttpInfo**](GroupsApi.md#getGroupWithHttpInfo) | **GET** /api/groups/{id} | Get a group by ID |
| [**getGroups**](GroupsApi.md#getGroups) | **GET** /api/groups | Get groups |
| [**getGroupsWithHttpInfo**](GroupsApi.md#getGroupsWithHttpInfo) | **GET** /api/groups | Get groups |
| [**updateGroup**](GroupsApi.md#updateGroup) | **PATCH** /api/groups/{id} | Update a group |
| [**updateGroupWithHttpInfo**](GroupsApi.md#updateGroupWithHttpInfo) | **PATCH** /api/groups/{id} | Update a group |



## createGroup

> Group createGroup(createGroupBody)

Create a group

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.GroupsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        GroupsApi apiInstance = new GroupsApi(defaultClient);
        CreateGroupBody createGroupBody = new CreateGroupBody(); // CreateGroupBody | 
        try {
            Group result = apiInstance.createGroup(createGroupBody);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling GroupsApi#createGroup");
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
| **createGroupBody** | [**CreateGroupBody**](CreateGroupBody.md)|  | |

### Return type

[**Group**](Group.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created group |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## createGroupWithHttpInfo

> ApiResponse<Group> createGroupWithHttpInfo(createGroupBody)

Create a group

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.GroupsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        GroupsApi apiInstance = new GroupsApi(defaultClient);
        CreateGroupBody createGroupBody = new CreateGroupBody(); // CreateGroupBody | 
        try {
            ApiResponse<Group> response = apiInstance.createGroupWithHttpInfo(createGroupBody);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling GroupsApi#createGroup");
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
| **createGroupBody** | [**CreateGroupBody**](CreateGroupBody.md)|  | |

### Return type

ApiResponse<[**Group**](Group.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created group |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## getGroup

> Group getGroup(id)

Get a group by ID

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.GroupsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        GroupsApi apiInstance = new GroupsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            Group result = apiInstance.getGroup(id);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling GroupsApi#getGroup");
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

[**Group**](Group.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Group |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## getGroupWithHttpInfo

> ApiResponse<Group> getGroupWithHttpInfo(id)

Get a group by ID

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.GroupsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        GroupsApi apiInstance = new GroupsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            ApiResponse<Group> response = apiInstance.getGroupWithHttpInfo(id);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling GroupsApi#getGroup");
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

ApiResponse<[**Group**](Group.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Group |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## getGroups

> GroupsListResponse getGroups()

Get groups

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.GroupsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        GroupsApi apiInstance = new GroupsApi(defaultClient);
        try {
            GroupsListResponse result = apiInstance.getGroups();
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling GroupsApi#getGroups");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**GroupsListResponse**](GroupsListResponse.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Groups list |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## getGroupsWithHttpInfo

> ApiResponse<GroupsListResponse> getGroupsWithHttpInfo()

Get groups

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.GroupsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        GroupsApi apiInstance = new GroupsApi(defaultClient);
        try {
            ApiResponse<GroupsListResponse> response = apiInstance.getGroupsWithHttpInfo();
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling GroupsApi#getGroups");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

ApiResponse<[**GroupsListResponse**](GroupsListResponse.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Groups list |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |


## updateGroup

> Group updateGroup(id, requestBody)

Update a group

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.GroupsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        GroupsApi apiInstance = new GroupsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        Map<String, Object> requestBody = null; // Map<String, Object> | 
        try {
            Group result = apiInstance.updateGroup(id, requestBody);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling GroupsApi#updateGroup");
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

[**Group**](Group.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Updated group |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## updateGroupWithHttpInfo

> ApiResponse<Group> updateGroupWithHttpInfo(id, requestBody)

Update a group

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.GroupsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        GroupsApi apiInstance = new GroupsApi(defaultClient);
        String id = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        Map<String, Object> requestBody = null; // Map<String, Object> | 
        try {
            ApiResponse<Group> response = apiInstance.updateGroupWithHttpInfo(id, requestBody);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling GroupsApi#updateGroup");
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

ApiResponse<[**Group**](Group.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Updated group |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

