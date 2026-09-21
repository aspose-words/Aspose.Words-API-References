---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType‑metod"
linktitle: "get_CssStyleSheetType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType‑metod. Anger hur CSS (Cascading Style Sheet)-stilar exporteras till HTML, MHTML eller EPUB. Standardvärdet är Inline för HTML/MHTML och External för EPUB i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheettype/
---
## HtmlSaveOptions::get_CssStyleSheetType method


Anger hur CSS (Cascading [Style](../../../aspose.words/style/) Sheet) stilar exporteras till HTML, MHTML eller EPUB. Standardvärdet är [Inline](../../cssstylesheettype/) för HTML/MHTML och [External](../../cssstylesheettype/) för EPUB.

```cpp
Aspose::Words::Saving::CssStyleSheetType Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType() const
```

## Anmärkningar


[Saving](../../) CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.

## Se även

* Enum [CssStyleSheetType](../../cssstylesheettype/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
