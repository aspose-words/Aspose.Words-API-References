---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias"
linktitle: "get_FontsFolderAlias"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias. Especifica el nombre de la carpeta utilizada para construir los URI de fuentes escritos en un documento HTML. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


Especifica el nombre de la carpeta utilizada para construir los URI de fuentes escritos en un documento HTML. El valor predeterminado es una cadena vacía.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## Observaciones


Cuando guardas un [Document](../../../aspose.words/document/) en formato HTML y [ExportFontResources](../get_exportfontresources/) está configurado en **true**, Aspose.Words necesita guardar las fuentes usadas en el documento como archivos independientes. [FontsFolder](../get_fontsfolder/) te permite especificar dónde se guardarán las fuentes y [FontsFolderAlias](./) permite especificar cómo se construirán los URI de las fuentes.

Si [FontsFolderAlias](./) no es una cadena vacía, entonces el URI de la fuente escrito en HTML será *FontsFolderAlias + <font file name>*.

Si [FontsFolderAlias](./) es una cadena vacía, entonces el URI de la fuente escrito en HTML será *FontsFolder + <font file name>*.

Si [FontsFolderAlias](./) se establece en '.' (punto), entonces el nombre del archivo de fuente se escribirá en HTML sin ruta, sin importar otras opciones.

Una forma alternativa de especificar el nombre de la carpeta para construir los URI de fuentes es usar [ResourceFolderAlias](../get_resourcefolderalias/).

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
