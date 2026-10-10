---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream método"
linktitle: "get_ResourceStream"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream método. Permite especificar el flujo donde se guardará el recurso en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


Permite especificar el flujo donde se guardará el recurso.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## Observaciones


Esta propiedad le permite guardar recursos en flujos en lugar de archivos.

El valor predeterminado es **null**. Cuando esta propiedad es **null**, el recurso se guardará en un archivo especificado en la propiedad [ResourceFileName](../get_resourcefilename/).

Al usar [IResourceSavingCallback](../../iresourcesavingcallback/) no puede sustituir un recurso por otro. Está destinado solo al control de la ubicación donde guardar los recursos.

## Ver también

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
