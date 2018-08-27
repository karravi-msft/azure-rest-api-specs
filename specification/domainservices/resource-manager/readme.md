# DomainServices

> see https://aka.ms/autorest

This is the AutoRest configuration file for DomainServices.



---
## Getting Started
To build the SDK for DomainServices, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information
These are the global settings for the DomainServices API.

``` yaml
openapi-type: arm
tag: package-2017-06
```

### Tag: package-2017-06

These settings apply only when `--tag=package-2017-06` is specified on the command line.

``` yaml $(tag) == 'package-2017-06'
input-file:
- Microsoft.AAD/stable/2017-06-01/domainservices.json
```

### Tag: package-2017-01

These settings apply only when `--tag=package-2017-01` is specified on the command line.

``` yaml $(tag) == 'package-2017-01'
input-file:
- Microsoft.AAD/stable/2017-01-01/domainservices.json
```

---
# Code Generation


## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-node
```

## C#

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.DomainServices
  payload-flattening-threshold: 2
  output-folder: $(csharp-sdks-folder)/DomainServices/Management.DomainServices/Generated
  clear-output-folder: true
```


## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: aad
  clear-output-folder: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2017-01
  - tag: package-2017-06
```

### Tag: package-2017-01 and go

These settings apply only when `--tag=package-2017-01 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2017-01' && $(go)
output-folder: $(go-sdk-folder)/services/domainservices/mgmt/2017-01-01/aad
```

### Tag: package-2017-06 and go

These settings apply only when `--tag=package-2017-01 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2017-06' && $(go)
output-folder: $(go-sdk-folder)/services/domainservices/mgmt/2017-06-01/aad
```

## Java

These settings apply only when `--java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-libraries-for-java clone>`.

``` yaml $(java)
azure-arm: true
fluent: true
namespace: com.microsoft.azure.management.domainservices
license-header: MICROSOFT_MIT_NO_CODEGEN
payload-flattening-threshold: 1
output-folder: $(azure-libraries-for-java-folder)/azure-mgmt-domainservices
```

### Java multi-api

``` yaml $(java) && $(multiapi)
batch:
  - tag: package-2017-06
  - tag: package-2017-01
```

### Tag: package-2017-06 and java

These settings apply only when `--tag=package-2017-06 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2017-06' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.domainservices.v2017_06_01
  output-folder: $(azure-libraries-for-java-folder)/domainservices/resource-manager/v2017_06_01
regenerate-manager: true
generate-interface: true
```

### Tag: package-2017-01 and java

These settings apply only when `--tag=package-2017-01 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2017-01' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.domainservices.v2017_01_01
  output-folder: $(azure-libraries-for-java-folder)/domainservices/resource-manager/v2017_01_01
regenerate-manager: true
generate-interface: true
```

