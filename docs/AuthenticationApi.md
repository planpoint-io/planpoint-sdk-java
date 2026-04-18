# AuthenticationApi

All URIs are relative to *https://app.planpoint.io*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**login**](AuthenticationApi.md#login) | **POST** /api/users/login | Login |
| [**loginWithHttpInfo**](AuthenticationApi.md#loginWithHttpInfo) | **POST** /api/users/login | Login |



## login

> AuthResponse login(loginBody)

Login

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.Configuration;
import io.planpoint.models.*;
import io.planpoint.api.AuthenticationApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");

        AuthenticationApi apiInstance = new AuthenticationApi(defaultClient);
        LoginBody loginBody = new LoginBody(); // LoginBody | 
        try {
            AuthResponse result = apiInstance.login(loginBody);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AuthenticationApi#login");
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
| **loginBody** | [**LoginBody**](LoginBody.md)|  | |

### Return type

[**AuthResponse**](AuthResponse.md)


### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Login successful |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

## loginWithHttpInfo

> ApiResponse<AuthResponse> loginWithHttpInfo(loginBody)

Login

### Example

```java
// Import classes:
import io.planpoint.ApiClient;
import io.planpoint.ApiException;
import io.planpoint.ApiResponse;
import io.planpoint.Configuration;
import io.planpoint.models.*;
import io.planpoint.api.AuthenticationApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://app.planpoint.io");

        AuthenticationApi apiInstance = new AuthenticationApi(defaultClient);
        LoginBody loginBody = new LoginBody(); // LoginBody | 
        try {
            ApiResponse<AuthResponse> response = apiInstance.loginWithHttpInfo(loginBody);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling AuthenticationApi#login");
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
| **loginBody** | [**LoginBody**](LoginBody.md)|  | |

### Return type

ApiResponse<[**AuthResponse**](AuthResponse.md)>


### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Login successful |  -  |
| **400** | Bad request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **405** | Method not allowed |  -  |
| **500** | Internal server error |  -  |

