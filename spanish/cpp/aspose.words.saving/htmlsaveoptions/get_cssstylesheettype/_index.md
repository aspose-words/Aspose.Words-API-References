---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType"
linktitle: "get_CssStyleSheetType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType. Especifica cómo se exportan los estilos CSS (Cascading Style Sheet) a HTML, MHTML o EPUB. El valor predeterminado es Inline para HTML/MHTML y External para EPUB en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheettype/
---
## HtmlSaveOptions::get_CssStyleSheetType method


Especifica cómo se exportan los estilos CSS (Cascading [Style](../../../aspose.words/style/) Sheet) a HTML, MHTML o EPUB. El valor predeterminado es [Inline](../../cssstylesheettype/) para HTML/MHTML y [External](../../cssstylesheettype/) para EPUB.

```cpp
Aspose::Words::Saving::CssStyleSheetType Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType() const
```

## Observaciones


[Saving](../../) CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.

## Ver también

* Enum [CssStyleSheetType](../../cssstylesheettype/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
