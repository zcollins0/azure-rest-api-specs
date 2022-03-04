# app

> see https://aka.ms/autorest

This is the AutoRest configuration file for Microsoft.App service.

## Getting Started

To build the SDKs for My API, simply install AutoRest via `npm` (`npm install -g autorest`) and then run:

> `autorest readme.md`

To see additional help and options, run:

> `autorest --help`

For other options on installation see [Installing AutoRest](https://aka.ms/autorest/install) on the AutoRest github page.

---

## Configuration

### Basic Information

These are the global settings for the app.

```yaml
openapi-type: arm
tag: package-2022-01-01-preview
```

### Tag: package-2022-01-01-preview

These settings apply only when `--tag=package-2022-01-01-preview` is specified on the command line.

```yaml $(tag) == 'package-2022-01-01-preview'
input-file:
  - Microsoft.App/preview/2022-01-01-preview/CommonDefinitions.json
  - Microsoft.App/preview/2022-01-01-preview/ContainerApps.json
  - Microsoft.App/preview/2022-01-01-preview/ContainerAppsRevisions.json
  - Microsoft.App/preview/2022-01-01-preview/ManagedEnvironments.json
  - Microsoft.App/preview/2022-01-01-preview/Global.json
  - Microsoft.App/preview/2022-01-01-preview/SourceControls.json
  - Microsoft.App/preview/2022-01-01-preview/DaprComponents.json
  - Microsoft.App/preview/2022-01-01-preview/AuthConfigs.json
  - Microsoft.App/preview/2022-01-01-preview/ManagedEnvironmentsStorages.json
directive:
- suppress: R4009
  from: ContainerAppsRevisions.json
  reason: False positive. This is not a tracked resource.
- suppress: R3010
  from: Global.json
  reason: False positive. The Revisions_list api already defined
- suppress: R3010
  from: ManagedEnvironments.json
  reason: False positive. The Revisions_list api already defined
- suppress: R3010
  from: ContainerAppsRevisions.json
  reason: False positive. The Revisions_list api already defined
- suppress: R3010
  from: CommonDefinitions.json
  reason: False positive. The Revisions_list api already defined
- suppress: R3010
  from: ContainerApps.json
  reason: False positive. The Revisions_list api already defined
- suppress: R3018
  from: Global.json
  reason: Use of boolean type is required
- suppress: R3018
  from: CommonDefinitions.json
  reason: Use of boolean type is required
- suppress: R3018
  from: ContainerApps.json
  reason: Use of boolean type is required
```

---

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

```yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-python-track2
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-go-track2
  - repo: azure-sdk-for-js
  - repo: azure-resource-manager-schemas
  - repo: azure-cli-extensions
```
## Az

See configuration in [readme.az.md](./readme.az.md)

## Go

See configuration in [readme.go.md](./readme.go.md)

## Python

See configuration in [readme.python.md](./readme.python.md)

## TypeScript

See configuration in [readme.typescript.md](./readme.typescript.md)

## CSharp

See configuration in [readme.csharp.md](./readme.csharp.md)