# WalletApi

All URIs are relative to *https://esi.tech.ccp.is*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCharactersCharacterIdWallet**](WalletApi.md#getCharactersCharacterIdWallet) | **GET** /v1/characters/{character_id}/wallet/ | Get a character&#39;s wallet balance
[**getCharactersCharacterIdWalletJournal**](WalletApi.md#getCharactersCharacterIdWalletJournal) | **GET** /v3/characters/{character_id}/wallet/journal/ | Get character wallet journal
[**getCharactersCharacterIdWalletTransactions**](WalletApi.md#getCharactersCharacterIdWalletTransactions) | **GET** /v1/characters/{character_id}/wallet/transactions/ | Get wallet transactions
[**getCorporationsCorporationIdWallets**](WalletApi.md#getCorporationsCorporationIdWallets) | **GET** /v1/corporations/{corporation_id}/wallets/ | Returns a corporation&#39;s wallet balance
[**getCorporationsCorporationIdWalletsDivisionJournal**](WalletApi.md#getCorporationsCorporationIdWalletsDivisionJournal) | **GET** /v2/corporations/{corporation_id}/wallets/{division}/journal/ | Get corporation wallet journal
[**getCorporationsCorporationIdWalletsDivisionTransactions**](WalletApi.md#getCorporationsCorporationIdWalletsDivisionTransactions) | **GET** /v1/corporations/{corporation_id}/wallets/{division}/transactions/ | Get corporation wallet transactions


<a name="getCharactersCharacterIdWallet"></a>
# **getCharactersCharacterIdWallet**
> Double getCharactersCharacterIdWallet(characterId, datasource, token, userAgent, xUserAgent)

Get a character&#39;s wallet balance

Returns a character&#39;s wallet balance  ---  This route is cached for up to 120 seconds

### Example
```java
// Import classes:
//import enterprises.orbital.eve.esi.client.invoker.ApiClient;
//import enterprises.orbital.eve.esi.client.invoker.ApiException;
//import enterprises.orbital.eve.esi.client.invoker.Configuration;
//import enterprises.orbital.eve.esi.client.invoker.auth.*;
//import enterprises.orbital.eve.esi.client.api.WalletApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: evesso
OAuth evesso = (OAuth) defaultClient.getAuthentication("evesso");
evesso.setAccessToken("YOUR ACCESS TOKEN");

WalletApi apiInstance = new WalletApi();
Integer characterId = 56; // Integer | An EVE character ID
String datasource = "tranquility"; // String | The server name you would like data from
String token = "token_example"; // String | Access token to use if unable to set a header
String userAgent = "userAgent_example"; // String | Client identifier, takes precedence over headers
String xUserAgent = "xUserAgent_example"; // String | Client identifier, takes precedence over User-Agent
try {
    Double result = apiInstance.getCharactersCharacterIdWallet(characterId, datasource, token, userAgent, xUserAgent);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WalletApi#getCharactersCharacterIdWallet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **characterId** | **Integer**| An EVE character ID |
 **datasource** | **String**| The server name you would like data from | [optional] [default to tranquility] [enum: tranquility, singularity]
 **token** | **String**| Access token to use if unable to set a header | [optional]
 **userAgent** | **String**| Client identifier, takes precedence over headers | [optional]
 **xUserAgent** | **String**| Client identifier, takes precedence over User-Agent | [optional]

### Return type

**Double**

### Authorization

[evesso](../README.md#evesso)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getCharactersCharacterIdWalletJournal"></a>
# **getCharactersCharacterIdWalletJournal**
> List&lt;GetCharactersCharacterIdWalletJournal200Ok&gt; getCharactersCharacterIdWalletJournal(characterId, datasource, fromId, token, userAgent, xUserAgent)

Get character wallet journal

Retrieve character wallet journal  ---  This route is cached for up to 3600 seconds  --- [This route has an available update](https://esi.tech.ccp.is/diff/latest/dev/#GET-/characters/{character_id}/wallet/journal/)

### Example
```java
// Import classes:
//import enterprises.orbital.eve.esi.client.invoker.ApiClient;
//import enterprises.orbital.eve.esi.client.invoker.ApiException;
//import enterprises.orbital.eve.esi.client.invoker.Configuration;
//import enterprises.orbital.eve.esi.client.invoker.auth.*;
//import enterprises.orbital.eve.esi.client.api.WalletApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: evesso
OAuth evesso = (OAuth) defaultClient.getAuthentication("evesso");
evesso.setAccessToken("YOUR ACCESS TOKEN");

WalletApi apiInstance = new WalletApi();
Integer characterId = 56; // Integer | An EVE character ID
String datasource = "tranquility"; // String | The server name you would like data from
Long fromId = 789L; // Long | Only show journal entries happened before the transaction referenced by this id
String token = "token_example"; // String | Access token to use if unable to set a header
String userAgent = "userAgent_example"; // String | Client identifier, takes precedence over headers
String xUserAgent = "xUserAgent_example"; // String | Client identifier, takes precedence over User-Agent
try {
    List<GetCharactersCharacterIdWalletJournal200Ok> result = apiInstance.getCharactersCharacterIdWalletJournal(characterId, datasource, fromId, token, userAgent, xUserAgent);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WalletApi#getCharactersCharacterIdWalletJournal");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **characterId** | **Integer**| An EVE character ID |
 **datasource** | **String**| The server name you would like data from | [optional] [default to tranquility] [enum: tranquility, singularity]
 **fromId** | **Long**| Only show journal entries happened before the transaction referenced by this id | [optional]
 **token** | **String**| Access token to use if unable to set a header | [optional]
 **userAgent** | **String**| Client identifier, takes precedence over headers | [optional]
 **xUserAgent** | **String**| Client identifier, takes precedence over User-Agent | [optional]

### Return type

[**List&lt;GetCharactersCharacterIdWalletJournal200Ok&gt;**](GetCharactersCharacterIdWalletJournal200Ok.md)

### Authorization

[evesso](../README.md#evesso)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getCharactersCharacterIdWalletTransactions"></a>
# **getCharactersCharacterIdWalletTransactions**
> List&lt;GetCharactersCharacterIdWalletTransactions200Ok&gt; getCharactersCharacterIdWalletTransactions(characterId, datasource, fromId, token, userAgent, xUserAgent)

Get wallet transactions

Get wallet transactions of a character  ---  This route is cached for up to 3600 seconds

### Example
```java
// Import classes:
//import enterprises.orbital.eve.esi.client.invoker.ApiClient;
//import enterprises.orbital.eve.esi.client.invoker.ApiException;
//import enterprises.orbital.eve.esi.client.invoker.Configuration;
//import enterprises.orbital.eve.esi.client.invoker.auth.*;
//import enterprises.orbital.eve.esi.client.api.WalletApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: evesso
OAuth evesso = (OAuth) defaultClient.getAuthentication("evesso");
evesso.setAccessToken("YOUR ACCESS TOKEN");

WalletApi apiInstance = new WalletApi();
Integer characterId = 56; // Integer | An EVE character ID
String datasource = "tranquility"; // String | The server name you would like data from
Long fromId = 789L; // Long | Only show transactions happened before the one referenced by this id
String token = "token_example"; // String | Access token to use if unable to set a header
String userAgent = "userAgent_example"; // String | Client identifier, takes precedence over headers
String xUserAgent = "xUserAgent_example"; // String | Client identifier, takes precedence over User-Agent
try {
    List<GetCharactersCharacterIdWalletTransactions200Ok> result = apiInstance.getCharactersCharacterIdWalletTransactions(characterId, datasource, fromId, token, userAgent, xUserAgent);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WalletApi#getCharactersCharacterIdWalletTransactions");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **characterId** | **Integer**| An EVE character ID |
 **datasource** | **String**| The server name you would like data from | [optional] [default to tranquility] [enum: tranquility, singularity]
 **fromId** | **Long**| Only show transactions happened before the one referenced by this id | [optional]
 **token** | **String**| Access token to use if unable to set a header | [optional]
 **userAgent** | **String**| Client identifier, takes precedence over headers | [optional]
 **xUserAgent** | **String**| Client identifier, takes precedence over User-Agent | [optional]

### Return type

[**List&lt;GetCharactersCharacterIdWalletTransactions200Ok&gt;**](GetCharactersCharacterIdWalletTransactions200Ok.md)

### Authorization

[evesso](../README.md#evesso)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getCorporationsCorporationIdWallets"></a>
# **getCorporationsCorporationIdWallets**
> List&lt;GetCorporationsCorporationIdWallets200Ok&gt; getCorporationsCorporationIdWallets(corporationId, datasource, token, userAgent, xUserAgent)

Returns a corporation&#39;s wallet balance

Get a corporation&#39;s wallets  ---  This route is cached for up to 300 seconds  --- Requires one of the following EVE corporation role(s): Accountant, Junior_Accountant

### Example
```java
// Import classes:
//import enterprises.orbital.eve.esi.client.invoker.ApiClient;
//import enterprises.orbital.eve.esi.client.invoker.ApiException;
//import enterprises.orbital.eve.esi.client.invoker.Configuration;
//import enterprises.orbital.eve.esi.client.invoker.auth.*;
//import enterprises.orbital.eve.esi.client.api.WalletApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: evesso
OAuth evesso = (OAuth) defaultClient.getAuthentication("evesso");
evesso.setAccessToken("YOUR ACCESS TOKEN");

WalletApi apiInstance = new WalletApi();
Integer corporationId = 56; // Integer | An EVE corporation ID
String datasource = "tranquility"; // String | The server name you would like data from
String token = "token_example"; // String | Access token to use if unable to set a header
String userAgent = "userAgent_example"; // String | Client identifier, takes precedence over headers
String xUserAgent = "xUserAgent_example"; // String | Client identifier, takes precedence over User-Agent
try {
    List<GetCorporationsCorporationIdWallets200Ok> result = apiInstance.getCorporationsCorporationIdWallets(corporationId, datasource, token, userAgent, xUserAgent);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WalletApi#getCorporationsCorporationIdWallets");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **corporationId** | **Integer**| An EVE corporation ID |
 **datasource** | **String**| The server name you would like data from | [optional] [default to tranquility] [enum: tranquility, singularity]
 **token** | **String**| Access token to use if unable to set a header | [optional]
 **userAgent** | **String**| Client identifier, takes precedence over headers | [optional]
 **xUserAgent** | **String**| Client identifier, takes precedence over User-Agent | [optional]

### Return type

[**List&lt;GetCorporationsCorporationIdWallets200Ok&gt;**](GetCorporationsCorporationIdWallets200Ok.md)

### Authorization

[evesso](../README.md#evesso)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getCorporationsCorporationIdWalletsDivisionJournal"></a>
# **getCorporationsCorporationIdWalletsDivisionJournal**
> List&lt;GetCorporationsCorporationIdWalletsDivisionJournal200Ok&gt; getCorporationsCorporationIdWalletsDivisionJournal(corporationId, division, datasource, fromId, token, userAgent, xUserAgent)

Get corporation wallet journal

Retrieve corporation wallet journal  ---  This route is cached for up to 3600 seconds  --- Requires one of the following EVE corporation role(s): Accountant, Junior_Accountant  --- [This route has an available update](https://esi.tech.ccp.is/diff/latest/dev/#GET-/corporations/{corporation_id}/wallets/{division}/journal/)

### Example
```java
// Import classes:
//import enterprises.orbital.eve.esi.client.invoker.ApiClient;
//import enterprises.orbital.eve.esi.client.invoker.ApiException;
//import enterprises.orbital.eve.esi.client.invoker.Configuration;
//import enterprises.orbital.eve.esi.client.invoker.auth.*;
//import enterprises.orbital.eve.esi.client.api.WalletApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: evesso
OAuth evesso = (OAuth) defaultClient.getAuthentication("evesso");
evesso.setAccessToken("YOUR ACCESS TOKEN");

WalletApi apiInstance = new WalletApi();
Integer corporationId = 56; // Integer | An EVE corporation ID
Integer division = 56; // Integer | Wallet key of the division to fetch journals from
String datasource = "tranquility"; // String | The server name you would like data from
Long fromId = 789L; // Long | Only show journal entries happened before the transaction referenced by this id
String token = "token_example"; // String | Access token to use if unable to set a header
String userAgent = "userAgent_example"; // String | Client identifier, takes precedence over headers
String xUserAgent = "xUserAgent_example"; // String | Client identifier, takes precedence over User-Agent
try {
    List<GetCorporationsCorporationIdWalletsDivisionJournal200Ok> result = apiInstance.getCorporationsCorporationIdWalletsDivisionJournal(corporationId, division, datasource, fromId, token, userAgent, xUserAgent);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WalletApi#getCorporationsCorporationIdWalletsDivisionJournal");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **corporationId** | **Integer**| An EVE corporation ID |
 **division** | **Integer**| Wallet key of the division to fetch journals from |
 **datasource** | **String**| The server name you would like data from | [optional] [default to tranquility] [enum: tranquility, singularity]
 **fromId** | **Long**| Only show journal entries happened before the transaction referenced by this id | [optional]
 **token** | **String**| Access token to use if unable to set a header | [optional]
 **userAgent** | **String**| Client identifier, takes precedence over headers | [optional]
 **xUserAgent** | **String**| Client identifier, takes precedence over User-Agent | [optional]

### Return type

[**List&lt;GetCorporationsCorporationIdWalletsDivisionJournal200Ok&gt;**](GetCorporationsCorporationIdWalletsDivisionJournal200Ok.md)

### Authorization

[evesso](../README.md#evesso)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getCorporationsCorporationIdWalletsDivisionTransactions"></a>
# **getCorporationsCorporationIdWalletsDivisionTransactions**
> List&lt;GetCorporationsCorporationIdWalletsDivisionTransactions200Ok&gt; getCorporationsCorporationIdWalletsDivisionTransactions(corporationId, division, datasource, fromId, token, userAgent, xUserAgent)

Get corporation wallet transactions

Get wallet transactions of a corporation  ---  This route is cached for up to 3600 seconds  --- Requires one of the following EVE corporation role(s): Accountant, Junior_Accountant

### Example
```java
// Import classes:
//import enterprises.orbital.eve.esi.client.invoker.ApiClient;
//import enterprises.orbital.eve.esi.client.invoker.ApiException;
//import enterprises.orbital.eve.esi.client.invoker.Configuration;
//import enterprises.orbital.eve.esi.client.invoker.auth.*;
//import enterprises.orbital.eve.esi.client.api.WalletApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: evesso
OAuth evesso = (OAuth) defaultClient.getAuthentication("evesso");
evesso.setAccessToken("YOUR ACCESS TOKEN");

WalletApi apiInstance = new WalletApi();
Integer corporationId = 56; // Integer | An EVE corporation ID
Integer division = 56; // Integer | Wallet key of the division to fetch journals from
String datasource = "tranquility"; // String | The server name you would like data from
Long fromId = 789L; // Long | Only show journal entries happened before the transaction referenced by this id
String token = "token_example"; // String | Access token to use if unable to set a header
String userAgent = "userAgent_example"; // String | Client identifier, takes precedence over headers
String xUserAgent = "xUserAgent_example"; // String | Client identifier, takes precedence over User-Agent
try {
    List<GetCorporationsCorporationIdWalletsDivisionTransactions200Ok> result = apiInstance.getCorporationsCorporationIdWalletsDivisionTransactions(corporationId, division, datasource, fromId, token, userAgent, xUserAgent);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WalletApi#getCorporationsCorporationIdWalletsDivisionTransactions");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **corporationId** | **Integer**| An EVE corporation ID |
 **division** | **Integer**| Wallet key of the division to fetch journals from |
 **datasource** | **String**| The server name you would like data from | [optional] [default to tranquility] [enum: tranquility, singularity]
 **fromId** | **Long**| Only show journal entries happened before the transaction referenced by this id | [optional]
 **token** | **String**| Access token to use if unable to set a header | [optional]
 **userAgent** | **String**| Client identifier, takes precedence over headers | [optional]
 **xUserAgent** | **String**| Client identifier, takes precedence over User-Agent | [optional]

### Return type

[**List&lt;GetCorporationsCorporationIdWalletsDivisionTransactions200Ok&gt;**](GetCorporationsCorporationIdWalletsDivisionTransactions200Ok.md)

### Authorization

[evesso](../README.md#evesso)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

