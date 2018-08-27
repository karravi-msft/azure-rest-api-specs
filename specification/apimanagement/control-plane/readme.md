# API Management Direct Control Plane Client
    
> see https://aka.ms/autorest

This is the AutoRest configuration file for Direct Control Plane SDK for API Management.



---
## Getting Started 
To build the SDK for API Management, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information 
These are the global settings for the API Management Direct Control Plane API.

``` yaml
openapi-type: default
tag: package-2017-03
```

### Tag: package-2017-03

These settings apply only when `--tag=package-2017-03` is specified on the command line.

``` yaml $(tag) == 'package-2017-03'
input-file:
- Microsoft.ApiManagement/preview/2017-03-01/apimanagement.json
- Microsoft.ApiManagement/preview/2017-03-01/apimapis.json
- Microsoft.ApiManagement/preview/2017-03-01/apimauthorizationservers.json
- Microsoft.ApiManagement/preview/2017-03-01/apimbackends.json
- Microsoft.ApiManagement/preview/2017-03-01/apimcertificates.json
- Microsoft.ApiManagement/preview/2017-03-01/apimemailtemplate.json
- Microsoft.ApiManagement/preview/2017-03-01/apimgroups.json
- Microsoft.ApiManagement/preview/2017-03-01/apimidentityprovider.json
- Microsoft.ApiManagement/preview/2017-03-01/apimloggers.json
- Microsoft.ApiManagement/preview/2017-03-01/apimopenidconnectproviders.json
- Microsoft.ApiManagement/preview/2017-03-01/apimportalsettings.json
- Microsoft.ApiManagement/preview/2017-03-01/apimproducts.json
- Microsoft.ApiManagement/preview/2017-03-01/apimproperties.json
- Microsoft.ApiManagement/preview/2017-03-01/apimquotas.json
- Microsoft.ApiManagement/preview/2017-03-01/apimreports.json
- Microsoft.ApiManagement/preview/2017-03-01/apimsubscriptions.json
- Microsoft.ApiManagement/preview/2017-03-01/apimtenant.json
- Microsoft.ApiManagement/preview/2017-03-01/apimusers.json
```

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-go
```

## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  clear-output-folder: true
  namespace: apimanagement
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2017-03
```

### Tag: package-2017-03 and go

These settings apply only when `--tag=package-2017-03 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2017-03' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/ctrl/2017-03-01/$(namespace)
```