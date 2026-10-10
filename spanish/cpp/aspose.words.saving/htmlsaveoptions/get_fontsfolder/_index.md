---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder"
linktitle: "get_FontsFolder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder. Especifica la carpeta física donde se guardan las fuentes al exportar un documento a HTML. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


Especifica la carpeta física donde se guardan las fuentes al exportar un documento a HTML. El valor predeterminado es una cadena vacía.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## Observaciones


Cuando guardas un [Document](../../../aspose.words/document/) en formato HTML y [ExportFontResources](../get_exportfontresources/) está configurado en **true**, Aspose.Words necesita guardar las fuentes usadas en el documento como archivos independientes. [FontsFolder](./) te permite especificar dónde se guardarán las fuentes y [FontsFolderAlias](../get_fontsfolderalias/) permite especificar cómo se construirán los URI de las fuentes.

Si guardas un documento en un archivo y proporcionas un nombre de archivo, Aspose.Words, por defecto, guarda las fuentes en la misma carpeta donde se guarda el archivo del documento. Usa [FontsFolder](./) para sobrescribir este comportamiento.

Si guardas un documento en un flujo, Aspose.Words no tiene una carpeta donde guardar las fuentes, pero aún necesita guardarlas en algún lugar. En este caso, debes especificar una carpeta accesible en la propiedad [FontsFolder](./) o proporcionar flujos personalizados a través del controlador de eventos [FontSavingCallback](../get_fontsavingcallback/).

Si la carpeta especificada por [FontsFolder](./) no existe, se creará automáticamente.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

## Ejemplos



Muestra cómo establecer carpetas y alias de carpetas para los recursos guardados externamente que Aspose.Words creará al guardar un documento en HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(get_ArtifactsDir() + u"Fonts");
options->set_ImagesFolder(get_ArtifactsDir() + u"Images");
options->set_ResourceFolder(get_ArtifactsDir() + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FolderAlias.html", options);
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
