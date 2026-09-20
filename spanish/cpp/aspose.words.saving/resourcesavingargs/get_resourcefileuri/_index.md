---
title: "Método Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri"
linktitle: "get_ResourceFileUri"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri. Obtiene o establece el identificador uniforme de recursos (URI) utilizado para referenciar el archivo de recurso desde el documento en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/resourcesavingargs/get_resourcefileuri/
---
## ResourceSavingArgs::get_ResourceFileUri method


Obtiene o establece el identificador uniforme de recursos (URI) utilizado para referenciar el archivo de recurso desde el documento.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri() const
```

## Observaciones


Esta propiedad le permite cambiar los URI de los archivos de recurso exportados a documentos HTML de página fija, SVG o Markdown.

Aspose.Words genera automáticamente un URI para cada archivo de recurso durante la exportación al formato HTML de página fija, SVG o Markdown. Los URI generados hacen referencia a los archivos de recurso guardados por Aspose.Words. Sin embargo, los URI pueden ser incorrectos si los archivos de recurso se trasladan a otra ubicación o si se guardan en flujos. Esta propiedad permite corregir los URI en estos casos.

Cuando se dispara el evento, esta propiedad contiene el URI que fue generado por Aspose.Words. Puede cambiar el valor de esta propiedad para proporcionar un URI personalizado para el archivo de recurso.
## Ver también

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
