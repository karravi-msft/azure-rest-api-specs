# Batch AI SDK

> see https://aka.ms/autorest

This is the AutoRest configuration file for Batch AI SDK.

---
## Getting Started
To build the SDK for Batch AI, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information
These are the global settings for the Batch AI.

``` yaml
openapi-type: arm
tag: package-2018-05
```


### Tag: package-2017-09-preview

These settings apply only when `--tag=package-2017-09-preview` is specified on the command line.

``` yaml $(tag) == 'package-2017-09-preview'
input-file:
- Microsoft.BatchAI/preview/2017-09-01-preview/BatchAI.json
```

### Tag: package-2018-03

These settings apply only when `--tag=package-2018-03` is specified on the command line.

``` yaml $(tag) == 'package-2018-03'
input-file:
- Microsoft.BatchAI/stable/2018-03-01/BatchAI.json
```

### Tag: package-2018-05

These settings apply only when `--tag=package-2018-05` is specified on the command line.

``` yaml $(tag) == 'package-2018-05'
input-file:
- Microsoft.BatchAI/stable/2018-05-01/BatchAI.json
```

---
# Code Generation


## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-node
```


## CSharp Settings

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.BatchAI
  payload-flattening-threshold: 1
  output-folder: $(csharp-sdks-folder)/BatchAI/Management.BatchAI/Generated
  clear-output-folder: true
```

## Python

These settings apply only when `--python` is specified on the command line.
Please also specify `--python-sdks-folder=<path to the root directory of your azure-sdk-for-python clone>`.
Use `--python-mode=update` if you already have a setup.py and just want to update the code itself.

``` yaml $(python)
python-mode: create
python:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  payload-flattening-threshold: 2
  namespace: azure.mgmt.batchai
  package-name: azure-mgmt-batchai
  clear-output-folder: true
```
``` yaml $(python) && $(python-mode) == 'update'
python:
  no-namespace-folders: true
  output-folder: $(python-sdks-folder)/azure-mgmt-batchai/azure/mgmt/batchai
```
``` yaml $(python) && $(python-mode) == 'create'
python:
  basic-setup-py: true
  output-folder: $(python-sdks-folder)/azure-mgmt-batchai
```

## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  clear-output-folder: true
  namespace: batchai
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2017-09-preview
  - tag: package-2018-03
  - tag: package-2018-05
```

### Tag: package-2017-09-preview and go

These settings apply only when `--tag=package-2017-09-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2017-09-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/batchai/mgmt/2017-09-preview/batchai
```

### Tag: package-2018-03 and go

These settings apply only when `--tag=package-2018-03 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2018-03' && $(go)
output-folder: $(go-sdk-folder)/services/batchai/mgmt/2018-03-01/batchai
```

### Tag: package-2018-05 and go

These settings apply only when `--tag=package-2018-05 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2018-05' && $(go)
output-folder: $(go-sdk-folder)/services/batchai/mgmt/2018-05-01/batchai
```

## Java

These settings apply only when `--java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-libraries-for-java clone>`.

``` yaml $(java)
azure-arm: true
fluent: true
namespace: com.microsoft.azure.management.batchai
license-header: MICROSOFT_MIT_NO_CODEGEN
payload-flattening-threshold: 1
output-folder: $(azure-libraries-for-java-folder)/azure-mgmt-batchai
```

### Java multi-api

``` yaml $(java) && $(multiapi)
batch:
  - tag: package-2017-09-preview
  - tag: package-2018-03
  - tag: package-2018-05
```

### Tag: package-2017-09-preview and java

These settings apply only when `--tag=package-2017-09-preview --java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag)=='package-2017-09-preview' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.batchai.v2017_09_01_preview
  output-folder: $(azure-libraries-for-java-folder)/batchai/resource-manager/v2017_09_01_preview
regenerate-manager: true
generate-interface: true
```

### Tag: package-2018-03 and java

These settings apply only when `--tag=package-2018-03 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag)=='package-2018-03' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.batchai.v2018_03_01
  output-folder: $(azure-libraries-for-java-folder)/batchai/resource-manager/v2018_03_01
regenerate-manager: true
generate-interface: true
```

### Tag: package-2018-05 and java

These settings apply only when `--tag=package-2018-05 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag)=='package-2018-05' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.batchai.v2018_05_01
  output-folder: $(azure-libraries-for-java-folder)/batchai/resource-manager/v2018_05_01
regenerate-manager: true
generate-interface: true
```