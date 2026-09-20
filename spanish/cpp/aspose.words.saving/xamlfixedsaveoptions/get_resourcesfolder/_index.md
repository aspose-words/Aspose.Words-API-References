---
title: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder método"
linktitle: "get_ResourcesFolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder método. Especifica la carpeta física donde se guardan los recursos (imágenes y fuentes) al exportar un documento al formato Xaml de página fija. El valor predeterminado es null en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/xamlfixedsaveoptions/get_resourcesfolder/
---
## XamlFixedSaveOptions::get_ResourcesFolder method


Especifica la carpeta física donde se guardan los recursos (imágenes y fuentes) al exportar un documento al formato Xaml de página fija. El valor predeterminado es **null**.

```cpp
System::String Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder() const
```

## Observaciones


Cuando guardas un [Document](../../../aspose.words/document/) en formato Xaml de página fija, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [ResourcesFolder](./) te permite especificar dónde se guardarán las imágenes y [ResourcesFolderAlias](../get_resourcesfolderalias/) permite especificar cómo se construirán los URI de las imágenes.

Si guardas un documento en un archivo y proporcionas un nombre de archivo, Aspose.Words, por defecto, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Usa [ResourcesFolder](./) para sobrescribir este comportamiento.

Si guardas un documento en un flujo, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aún necesita guardarlas en algún lugar. En este caso, debes especificar una carpeta accesible usando la propiedad [ResourcesFolder](./).

## Ver también

* Class [XamlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
