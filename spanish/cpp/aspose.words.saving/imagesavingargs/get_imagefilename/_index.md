---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName método"
linktitle: "get_ImageFileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName método. Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la imagen en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la imagen.

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## Observaciones


Esta propiedad le permite redefinir cómo se generan los nombres de archivo de imagen durante la exportación a HTML.

Cuando se dispara el evento, esta propiedad contiene el nombre de archivo que fue generado por Aspose.Words. Puede cambiar el valor de esta propiedad para guardar la imagen en un archivo diferente. Tenga en cuenta que los nombres de archivo deben ser únicos.

Aspose.Words genera automáticamente un nombre de archivo único para cada imagen incrustada al exportar al formato HTML. Cómo se genera el nombre de archivo de la imagen depende de si guarda el documento en un archivo o en un flujo.

Al guardar un documento en un archivo, el nombre de archivo de imagen generado tiene el aspecto *%<document base file name>.<image number>.<extension>*.

Al guardar un documento en un flujo, el nombre de archivo de imagen generado tiene el aspecto *Aspose.Words.<document guid>.<image number>.<extension>*.

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## Ver también

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
