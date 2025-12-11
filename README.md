# Cloudmersive.APIClient.NETCore.CDR - the C# library for the CDR API

Use the Content Disarm and Reconstruction API to remove security risks from documents by tearing them down, removing unsafe content and rebuilding them.

This C# SDK is for the [Cloudmersive Content Disarm and Reconstruction API](https://www.cloudmersive.com/cdr-api):

- API version: v1
- SDK version: 2.1.0
- Build package: io.swagger.codegen.languages.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET Core >=1.0
- .NET Framework >=4.6
- Mono/Xamarin >=vNext
- UWP >=10.0

<a name="dependencies"></a>
## Dependencies
- FubarCoder.RestSharp.Portable.Core >=4.0.7
- FubarCoder.RestSharp.Portable.HttpClient >=4.0.7
- Newtonsoft.Json >=10.0.3

<a name="installation"></a>
## Installation
Generate the DLL using your preferred tool

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using Cloudmersive.APIClient.NETCore.CDR.Api;
using Cloudmersive.APIClient.NETCore.CDR.Client;
using Cloudmersive.APIClient.NETCore.CDR.Model;
```
<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.CDR.Api;
using Cloudmersive.APIClient.NETCore.CDR.Client;
using Cloudmersive.APIClient.NETCore.CDR.Model;

namespace Example
{
    public class Example
    {
        public void main()
        {

            // Configure API key authorization: Apikey
            Configuration.Default.ApiKey.Add("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Apikey", "Bearer");

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

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://api.cloudmersive.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*FileSanitizationApi* | [**CallFile**](docs/FileSanitizationApi.md#callfile) | **POST** /cdr/sanitization/file | Content Disarm and Reconstruction on a File
*FileSanitizationApi* | [**FileToPdf**](docs/FileSanitizationApi.md#filetopdf) | **POST** /cdr/sanitization/file/to/pdf | Content Disarm and Reconstruction on a File with PDFA Output


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.ProblemDetails](docs/ProblemDetails.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="Apikey"></a>
### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

