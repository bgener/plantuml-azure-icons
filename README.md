# Overview

The PlantUML offers a great way to speed-up creation of architectural diagrams. However, the default rendering might look overwhelming and noisy for non-technical people. Using familiar icons, helps them to understand the diagram without knowing the UML.

This repository demonstrates how to use plantuml with custom images, i.e. Azure icons. Unlike other solutions, here we do not use sprites, but png images.

## Getting started

Navigate to [PlantText WebSite](planttext.com) and use the following snippet:

``` bash
skinparam monochrome true
skinparam defaultTextAlignment center

!define Url https://raw.githubusercontent.com/bgener/plantuml-azure-icons/master/images
rectangle "<img Url/AzureAPIManagement.png>\nAPI Management" as apim
rectangle "<img Url/AzureFunctions.png>\n...\n<img Url/AzureFunctions.png>\nAzure Funcs" as backend
actor Client

Client -> apim
apim -right-> backend
apim -right-> backend
```

This will render the diagram as shown:
![Getting Started](docs\getting-started.png)

## Resources

* [PlantUML guide](http://plantuml.com/guide)
* [Azure-PlantUML with sprites](https://github.com/RicardoNiepel/Azure-PlantUML)