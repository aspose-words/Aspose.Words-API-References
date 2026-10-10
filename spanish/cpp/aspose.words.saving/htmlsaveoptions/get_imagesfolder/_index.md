---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder método"
linktitle: "get_ImagesFolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder método. Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato HTML. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 38000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato HTML. El valor predeterminado es una cadena vacía.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## Observaciones


Cuando guardas un [Document](../../../aspose.words/document/) en formato HTML, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [ImagesFolder](./) te permite especificar dónde se guardarán las imágenes y [ImagesFolderAlias](../get_imagesfolderalias/) permite especificar cómo se construirán los URI de las imágenes.

Si guardas un documento en un archivo y proporcionas un nombre de archivo, Aspose.Words, por defecto, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Usa [ImagesFolder](./) para sobrescribir este comportamiento.

Si guardas un documento en un flujo, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aún necesita guardarlas en algún lugar. En este caso, debes especificar una carpeta accesible en la propiedad [ImagesFolder](./) o proporcionar flujos personalizados a través del controlador de eventos [ImageSavingCallback](../get_imagesavingcallback/).

Si la carpeta especificada por [ImagesFolder](./) no existe, se creará automáticamente.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

## Ejemplos



Muestra cómo especificar la carpeta para almacenar imágenes vinculadas después de guardar en .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Establece una opción para exportar los campos de formulario como texto plano en lugar de elementos de entrada HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
