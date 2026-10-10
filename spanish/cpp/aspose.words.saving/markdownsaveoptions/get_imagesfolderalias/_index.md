---
title: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias"
linktitle: "get_ImagesFolderAlias"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias. Especifica el nombre de la carpeta utilizada para construir los URI de imágenes escritos en un documento. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 5500
url: /es/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


Especifica el nombre de la carpeta utilizada para construir los URI de imágenes escritos en un documento. El valor predeterminado es una cadena vacía.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## Observaciones


Cuando guardas un [Document](../../../aspose.words/document/) en formato [Markdown](../../../aspose.words/saveformat/), Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [ImagesFolder](../get_imagesfolder/) te permite especificar dónde se guardarán las imágenes y [ImagesFolderAlias](./) permite especificar cómo se construirán los URI de las imágenes.

Si [ImagesFolderAlias](./) no es una cadena vacía, entonces el URI de la imagen escrito en Markdown será *ImagesFolderAlias + <image file name>*.

Si [ImagesFolderAlias](./) es una cadena vacía, entonces el URI de la imagen escrito en Markdown será *ImagesFolder + <image file name>*.

Si [ImagesFolderAlias](./) está configurado a '.' (punto), entonces el nombre del archivo de imagen se escribirá en Markdown sin ruta, sin importar otras opciones.

## Ejemplos



Muestra cómo especificar el nombre de la carpeta utilizada para construir los URI de imágenes.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// Usa la propiedad \"ImagesFolder\" para asignar una carpeta en el sistema de archivos local en la que
// Aspose.Words guardará todas las imágenes vinculadas del documento.
saveOptions->set_ImagesFolder(imagesFolder);
// Usa la propiedad \"ImagesFolderAlias\" para usar esta carpeta
// al construir los URI de imágenes en lugar del nombre de la carpeta de imágenes.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## Ver también

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
