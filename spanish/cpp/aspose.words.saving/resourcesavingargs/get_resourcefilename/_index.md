---
title: "Método Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName"
linktitle: "get_ResourceFileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName. Obtiene o establece el nombre de archivo (sin ruta) donde se guardará el recurso en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


Obtiene o establece el nombre de archivo (sin ruta) donde se guardará el recurso.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## Observaciones


Esta propiedad le permite redefinir cómo se generan los nombres de archivo de recursos durante la exportación a HTML de página fija, SVG o Markdown.

Cuando se dispara el evento, esta propiedad contiene el nombre de archivo que fue generado por Aspose.Words. Puede cambiar el valor de esta propiedad para guardar el recurso en un archivo diferente. Tenga en cuenta que los nombres de archivo deben ser únicos.

Aspose.Words genera automáticamente un nombre de archivo único para cada recurso al exportar al formato HTML de página fija, SVG o Markdown. Cómo se genera el nombre de archivo del recurso depende de si guarda el documento en un archivo o en un flujo.

Al guardar un documento en un archivo, el nombre de archivo de recurso generado tiene el aspecto *%<document base file name>.<image number>.<extension>*.

Al guardar un documento en un flujo, el nombre de archivo de recurso generado tiene el aspecto *Aspose.Words.<document guid>.<image number>.<extension>*.

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## Ver también

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
