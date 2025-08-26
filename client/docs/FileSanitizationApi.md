# Cloudmersive.APIClient.NETCore.CDR.Api.FileSanitizationApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CallFile**](FileSanitizationApi.md#callfile) | **POST** /cdr/sanitization/file | Complete Content Disarm and Reconstruction on an Input File, and output in same file format
[**FileToPdf**](FileSanitizationApi.md#filetopdf) | **POST** /cdr/sanitization/file/to/pdf | Complete Content Disarm and Reconstruction on an Input File with PDF/A Output


<a name="callfile"></a>
# **CallFile**
> void CallFile (System.IO.Stream inputFile = null)

Complete Content Disarm and Reconstruction on an Input File, and output in same file format

Processes the input file via CDR to produce a secured output file.  Input content is parsed, disarmed, and then reconstructed into a new output file with the same file format as the input.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.CDR.Api;
using Cloudmersive.APIClient.NETCore.CDR.Client;
using Cloudmersive.APIClient.NETCore.CDR.Model;

namespace Example
{
    public class CallFileExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new FileSanitizationApi();
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Complete Content Disarm and Reconstruction on an Input File, and output in same file format
                apiInstance.CallFile(inputFile);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling FileSanitizationApi.CallFile: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

void (empty response body)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="filetopdf"></a>
# **FileToPdf**
> void FileToPdf (System.IO.Stream inputFile = null)

Complete Content Disarm and Reconstruction on an Input File with PDF/A Output

Processes the input file via CDR to produce a secured PDF/A output file.  Input content is parsed, disarmed, and then reconstructed into a new PDF/A output file.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.CDR.Api;
using Cloudmersive.APIClient.NETCore.CDR.Client;
using Cloudmersive.APIClient.NETCore.CDR.Model;

namespace Example
{
    public class FileToPdfExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new FileSanitizationApi();
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Complete Content Disarm and Reconstruction on an Input File with PDF/A Output
                apiInstance.FileToPdf(inputFile);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling FileSanitizationApi.FileToPdf: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

void (empty response body)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

