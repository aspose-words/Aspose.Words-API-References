---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder método"
linktitle: "get_ImagesFolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder método. Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato XAML. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato XAML. El valor predeterminado es una cadena vacía.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## Observaciones


Cuando guardas un [Document](../../../aspose.words/document/) en formato XAML, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [ImagesFolder](./) te permite especificar dónde se guardarán las imágenes y [ImagesFolderAlias](../get_imagesfolderalias/) permite especificar cómo se construirán los URI de las imágenes.

Si guardas un documento en un archivo y proporcionas un nombre de archivo, Aspose.Words, por defecto, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Usa [ImagesFolder](./) para sobrescribir este comportamiento.

Si guardas un documento en un flujo, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aún necesita guardarlas en algún lugar. En este caso, debes especificar una carpeta accesible en la propiedad [ImagesFolder](./) o proporcionar flujos personalizados a través del controlador de eventos [ImageSavingCallback](../get_imagesavingcallback/).

## Ver también

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
