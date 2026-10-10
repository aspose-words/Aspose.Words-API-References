---
title: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType"
linktitle: "get_CssStyleSheetType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType. Specifica come gli stili CSS (Cascading Style Sheet) vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è Inline per HTML/MHTML ed External per EPUB in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheettype/
---
## HtmlSaveOptions::get_CssStyleSheetType method


Specifica come gli stili CSS (Cascading [Style](../../../aspose.words/style/) Sheet) vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è [Inline](../../cssstylesheettype/) per HTML/MHTML e [External](../../cssstylesheettype/) per EPUB.

```cpp
Aspose::Words::Saving::CssStyleSheetType Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType() const
```

## Note


[Saving](../../) CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.

## Vedi anche

* Enum [CssStyleSheetType](../../cssstylesheettype/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
