# Cloudmersive.APIClient.NETCore.CDR.Api.FileSanitizationApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CallFile**](FileSanitizationApi.md#callfile) | **POST** /cdr/sanitization/file | Content Disarm and Reconstruction on a File
[**FileAdvanced**](FileSanitizationApi.md#fileadvanced) | **POST** /cdr/sanitization/file/advanced | Advanced Content Disarm and Reconstruction on a File
[**FileToPdf**](FileSanitizationApi.md#filetopdf) | **POST** /cdr/sanitization/file/to/pdf | Content Disarm and Reconstruction on a File with PDFA Output
[**FileToPdfAdvanced**](FileSanitizationApi.md#filetopdfadvanced) | **POST** /cdr/sanitization/file/to/pdf/advanced | Advanced Content Disarm and Reconstruction on a File with PDFA Output


<a name="callfile"></a>
# **CallFile**
> byte[] CallFile (System.IO.Stream inputFile = null)

Content Disarm and Reconstruction on a File

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
                // Content Disarm and Reconstruction on a File
                byte[] result = apiInstance.CallFile(inputFile);
                Debug.WriteLine(result);
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

**byte[]**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="fileadvanced"></a>
# **FileAdvanced**
> byte[] FileAdvanced (bool? allowExecutables = null, bool? allowInvalidFiles = null, bool? allowScripts = null, bool? allowPasswordProtectedFiles = null, bool? allowMacros = null, bool? allowXmlExternalEntities = null, bool? allowInsecureDeserialization = null, bool? allowHtml = null, bool? allowUnsafeArchives = null, bool? allowOleEmbeddedObject = null, bool? allowUnwantedAction = null, string restrictFileTypes = null, System.IO.Stream inputFile = null)

Advanced Content Disarm and Reconstruction on a File

Processes the input file via CDR to produce a secured output file with advanced scan options and response headers containing scan metadata.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.CDR.Api;
using Cloudmersive.APIClient.NETCore.CDR.Client;
using Cloudmersive.APIClient.NETCore.CDR.Model;

namespace Example
{
    public class FileAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new FileSanitizationApi();
            var allowExecutables = true;  // bool? | Set to false to block executable files (EXE, DLL, etc.) (optional) 
            var allowInvalidFiles = true;  // bool? | Set to false to block files that are not valid for their detected type (optional) 
            var allowScripts = true;  // bool? | Set to false to block script files. PDF and Office macro sanitization still runs regardless. (optional) 
            var allowPasswordProtectedFiles = true;  // bool? | Set to false to block password-protected files (optional) 
            var allowMacros = true;  // bool? | Set to false to block files containing macros. Office macro removal still runs regardless. (optional) 
            var allowXmlExternalEntities = true;  // bool? | Set to false to block XML files with external entity references (XXE) (optional) 
            var allowInsecureDeserialization = true;  // bool? | Set to false to block files with insecure deserialization patterns (optional) 
            var allowHtml = true;  // bool? | Set to false to block HTML files (optional) 
            var allowUnsafeArchives = true;  // bool? | Set to false to block archive files flagged as unsafe (e.g., zip bombs) (optional) 
            var allowOleEmbeddedObject = true;  // bool? | Set to false to block files with embedded OLE objects (optional) 
            var allowUnwantedAction = true;  // bool? | Set to false to block files with unwanted actions (optional) 
            var restrictFileTypes = restrictFileTypes_example;  // string | Comma-separated list of allowed file extensions (e.g., \".pdf,.docx,.xlsx\"). Files not matching will be blocked. (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document to CDR process (optional) 

            try
            {
                // Advanced Content Disarm and Reconstruction on a File
                byte[] result = apiInstance.FileAdvanced(allowExecutables, allowInvalidFiles, allowScripts, allowPasswordProtectedFiles, allowMacros, allowXmlExternalEntities, allowInsecureDeserialization, allowHtml, allowUnsafeArchives, allowOleEmbeddedObject, allowUnwantedAction, restrictFileTypes, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling FileSanitizationApi.FileAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowExecutables** | **bool?**| Set to false to block executable files (EXE, DLL, etc.) | [optional] 
 **allowInvalidFiles** | **bool?**| Set to false to block files that are not valid for their detected type | [optional] 
 **allowScripts** | **bool?**| Set to false to block script files. PDF and Office macro sanitization still runs regardless. | [optional] 
 **allowPasswordProtectedFiles** | **bool?**| Set to false to block password-protected files | [optional] 
 **allowMacros** | **bool?**| Set to false to block files containing macros. Office macro removal still runs regardless. | [optional] 
 **allowXmlExternalEntities** | **bool?**| Set to false to block XML files with external entity references (XXE) | [optional] 
 **allowInsecureDeserialization** | **bool?**| Set to false to block files with insecure deserialization patterns | [optional] 
 **allowHtml** | **bool?**| Set to false to block HTML files | [optional] 
 **allowUnsafeArchives** | **bool?**| Set to false to block archive files flagged as unsafe (e.g., zip bombs) | [optional] 
 **allowOleEmbeddedObject** | **bool?**| Set to false to block files with embedded OLE objects | [optional] 
 **allowUnwantedAction** | **bool?**| Set to false to block files with unwanted actions | [optional] 
 **restrictFileTypes** | **string**| Comma-separated list of allowed file extensions (e.g., \&quot;.pdf,.docx,.xlsx\&quot;). Files not matching will be blocked. | [optional] 
 **inputFile** | **System.IO.Stream**| Input document to CDR process | [optional] 

### Return type

**byte[]**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="filetopdf"></a>
# **FileToPdf**
> byte[] FileToPdf (System.IO.Stream inputFile = null)

Content Disarm and Reconstruction on a File with PDFA Output

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
                // Content Disarm and Reconstruction on a File with PDFA Output
                byte[] result = apiInstance.FileToPdf(inputFile);
                Debug.WriteLine(result);
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

**byte[]**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="filetopdfadvanced"></a>
# **FileToPdfAdvanced**
> byte[] FileToPdfAdvanced (bool? allowExecutables = null, bool? allowInvalidFiles = null, bool? allowScripts = null, bool? allowPasswordProtectedFiles = null, bool? allowMacros = null, bool? allowXmlExternalEntities = null, bool? allowInsecureDeserialization = null, bool? allowHtml = null, bool? allowUnsafeArchives = null, bool? allowOleEmbeddedObject = null, bool? allowUnwantedAction = null, string restrictFileTypes = null, System.IO.Stream inputFile = null)

Advanced Content Disarm and Reconstruction on a File with PDFA Output

Processes the input file via CDR to produce a secured PDF/A output file with advanced scan options and response headers containing scan metadata.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.CDR.Api;
using Cloudmersive.APIClient.NETCore.CDR.Client;
using Cloudmersive.APIClient.NETCore.CDR.Model;

namespace Example
{
    public class FileToPdfAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new FileSanitizationApi();
            var allowExecutables = true;  // bool? | Set to false to block executable files (EXE, DLL, etc.) (optional) 
            var allowInvalidFiles = true;  // bool? | Set to false to block files that are not valid for their detected type (optional) 
            var allowScripts = true;  // bool? | Set to false to block script files. PDF and Office macro sanitization still runs regardless. (optional) 
            var allowPasswordProtectedFiles = true;  // bool? | Set to false to block password-protected files (optional) 
            var allowMacros = true;  // bool? | Set to false to block files containing macros. Office macro removal still runs regardless. (optional) 
            var allowXmlExternalEntities = true;  // bool? | Set to false to block XML files with external entity references (XXE) (optional) 
            var allowInsecureDeserialization = true;  // bool? | Set to false to block files with insecure deserialization patterns (optional) 
            var allowHtml = true;  // bool? | Set to false to block HTML files (optional) 
            var allowUnsafeArchives = true;  // bool? | Set to false to block archive files flagged as unsafe (e.g., zip bombs) (optional) 
            var allowOleEmbeddedObject = true;  // bool? | Set to false to block files with embedded OLE objects (optional) 
            var allowUnwantedAction = true;  // bool? | Set to false to block files with unwanted actions (optional) 
            var restrictFileTypes = restrictFileTypes_example;  // string | Comma-separated list of allowed file extensions (e.g., \".pdf,.docx,.xlsx\"). Files not matching will be blocked. (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document to CDR process (optional) 

            try
            {
                // Advanced Content Disarm and Reconstruction on a File with PDFA Output
                byte[] result = apiInstance.FileToPdfAdvanced(allowExecutables, allowInvalidFiles, allowScripts, allowPasswordProtectedFiles, allowMacros, allowXmlExternalEntities, allowInsecureDeserialization, allowHtml, allowUnsafeArchives, allowOleEmbeddedObject, allowUnwantedAction, restrictFileTypes, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling FileSanitizationApi.FileToPdfAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowExecutables** | **bool?**| Set to false to block executable files (EXE, DLL, etc.) | [optional] 
 **allowInvalidFiles** | **bool?**| Set to false to block files that are not valid for their detected type | [optional] 
 **allowScripts** | **bool?**| Set to false to block script files. PDF and Office macro sanitization still runs regardless. | [optional] 
 **allowPasswordProtectedFiles** | **bool?**| Set to false to block password-protected files | [optional] 
 **allowMacros** | **bool?**| Set to false to block files containing macros. Office macro removal still runs regardless. | [optional] 
 **allowXmlExternalEntities** | **bool?**| Set to false to block XML files with external entity references (XXE) | [optional] 
 **allowInsecureDeserialization** | **bool?**| Set to false to block files with insecure deserialization patterns | [optional] 
 **allowHtml** | **bool?**| Set to false to block HTML files | [optional] 
 **allowUnsafeArchives** | **bool?**| Set to false to block archive files flagged as unsafe (e.g., zip bombs) | [optional] 
 **allowOleEmbeddedObject** | **bool?**| Set to false to block files with embedded OLE objects | [optional] 
 **allowUnwantedAction** | **bool?**| Set to false to block files with unwanted actions | [optional] 
 **restrictFileTypes** | **string**| Comma-separated list of allowed file extensions (e.g., \&quot;.pdf,.docx,.xlsx\&quot;). Files not matching will be blocked. | [optional] 
 **inputFile** | **System.IO.Stream**| Input document to CDR process | [optional] 

### Return type

**byte[]**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

