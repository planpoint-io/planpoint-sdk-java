# LeadsApi

All URIs are relative to *https://app.planpoint.io*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getLeads**](LeadsApi.md#getLeads) | **GET** /api/leads | Get leads for a project |
| [**getLeadsWithHttpInfo**](LeadsApi.md#getLeadsWithHttpInfo) | **GET** /api/leads | Get leads for a project |



## getLeads

> List<Lead> getLeads(pid)

Get leads for a project

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.LeadsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        LeadsApi apiInstance = new LeadsApi(defaultClient);
        String pid = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            List<Lead> result = apiInstance.getLeads(pid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling LeadsApi#getLeads");
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

[**List&lt;Lead&gt;**](Lead.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Leads list |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## getLeadsWithHttpInfo

> ApiResponse<List<Lead>> getLeadsWithHttpInfo(pid)

Get leads for a project

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.auth.*;
import io.planpoint.models.*;
import io.planpoint.api.LeadsApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        LeadsApi apiInstance = new LeadsApi(defaultClient);
        String pid = "64a1f2b3c4d5e6f7a8b9c0d1"; // String | 
        try {
            ApiResponse<List<Lead>> response = apiInstance.getLeadsWithHttpInfo(pid);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling LeadsApi#getLeads");
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

ApiResponse<[**List&lt;Lead&gt;**](Lead.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Leads list |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

