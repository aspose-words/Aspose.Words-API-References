---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method"
linktitle: "get_CssStyleSheetFileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method. Especifica la ruta y el nombre del archivo de hoja de estilo en cascada (CSS) que se escribe cuando un documento se exporta a HTML. El valor predeterminado es una cadena vacía en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


Especifica la ruta y el nombre del archivo de hoja de estilo en cascada [Style](../../../aspose.words/style/) (CSS) que se escribe cuando un documento se exporta a HTML. El valor predeterminado es una cadena vacía.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## Observaciones


Esta propiedad tiene efecto solo al guardar un documento en formato HTML y se solicita una hoja de estilo CSS externa usando [CssStyleSheetType](../get_cssstylesheettype/).

Si esta propiedad está vacía, el archivo CSS se guardará en la misma carpeta y con el mismo nombre que el documento HTML pero con la extensión ".css".

Si solo se especifica la ruta pero no el nombre de archivo en esta propiedad, el archivo CSS se guardará en la carpeta especificada y tendrá el mismo nombre que el documento HTML pero con la extensión ".css".

Si la carpeta especificada por esta propiedad no existe, se creará automáticamente antes de guardar el archivo CSS.

Otra forma de especificar una carpeta donde se guarda el archivo CSS externo es usar [ResourceFolder](../get_resourcefolder/).

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
