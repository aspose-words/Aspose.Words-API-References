---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias método"
linktitle: "get_ImagesFolderAlias"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias método. Especifica el nombre de la carpeta utilizada para construir los URI de imágenes escritos en un documento XAML. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


Especifica el nombre de la carpeta utilizada para construir los URI de imágenes escritos en un documento XAML. El valor predeterminado es una cadena vacía.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## Observaciones


Cuando guardas un [Document](../../../aspose.words/document/) en formato XAML, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [ImagesFolder](../get_imagesfolder/) te permite especificar dónde se guardarán las imágenes y [ImagesFolderAlias](./) permite especificar cómo se construirán los URI de las imágenes.

Si [ImagesFolderAlias](./) no es una cadena vacía, entonces el URI de la imagen escrito en XAML será *ImagesFolderAlias + <image file name>*.

Si [ImagesFolderAlias](./) es una cadena vacía, entonces el URI de la imagen escrito en XAML será *ImagesFolder + <image file name>*.

Si [ImagesFolderAlias](./) se establece en '.' (punto), entonces el nombre del archivo de imagen se escribirá en XAML sin ruta, sin importar otras opciones.

## Ver también

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
