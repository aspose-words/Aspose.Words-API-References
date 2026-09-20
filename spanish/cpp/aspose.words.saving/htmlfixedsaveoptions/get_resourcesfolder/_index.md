---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder método"
linktitle: "get_ResourcesFolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder método. Especifica la carpeta física donde se guardan los recursos (imágenes, fuentes, css) al exportar un documento al formato Html. El valor predeterminado es null en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_resourcesfolder/
---
## HtmlFixedSaveOptions::get_ResourcesFolder method


Especifica la carpeta física donde se guardan los recursos (imágenes, fuentes, css) al exportar un documento al formato Html. El valor predeterminado es **null**.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder() const
```

## Observaciones


Solo tiene efecto si la propiedad [ExportEmbeddedImages](../get_exportembeddedimages/) es **false**.

Cuando guardas un [Document](../../../aspose.words/document/) en formato Html, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [ResourcesFolder](./) te permite especificar dónde se guardarán las imágenes y [ResourcesFolderAlias](../get_resourcesfolderalias/) permite especificar cómo se construirán los URI de las imágenes.

Si guardas un documento en un archivo y proporcionas un nombre de archivo, Aspose.Words, por defecto, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Usa [ResourcesFolder](./) para sobrescribir este comportamiento.

Si guardas un documento en un flujo, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aún necesita guardarlas en algún lugar. En este caso, debes especificar una carpeta accesible usando la propiedad [ResourcesFolder](./).

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
