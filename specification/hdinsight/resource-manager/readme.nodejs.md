## Node.js

These settings apply only when `--nodejs` is specified on the command line.
Please also specify `--node-sdks-folder=<path to root folder of your azure-sdk-for-node clone>`.

``` yaml $(nodejs)
nodejs:
  azure-arm: true
  package-name: azure-arm-hdinsight
  package-version: 0.6.0
  output-folder: $(node-sdks-folder)/lib/services/hdInsightManagement
  generate-license-txt: true
  generate-package-json: true
  generate-readme-md: true
```