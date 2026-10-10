---
title: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder"
linktitle: "get_ImagesFolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder método. Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato Markdown. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato [Markdown](../../../aspose.words/saveformat/). El valor predeterminado es una cadena vacía.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## Observaciones


Al guardar un [Document](../../../aspose.words/document/) en formato [Markdown](../../../aspose.words/saveformat/), Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [ImagesFolder](./) le permite especificar dónde se guardarán las imágenes.

Si guardas un documento en un archivo y proporcionas un nombre de archivo, Aspose.Words, por defecto, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Usa [ImagesFolder](./) para sobrescribir este comportamiento.

Si guarda un documento en un flujo, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aún necesita guardarlas en algún lugar. En este caso, debe especificar una carpeta accesible en la propiedad [ImagesFolder](./).

Si la carpeta especificada por [ImagesFolder](./) no existe, se creará automáticamente.

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
