---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType yöntemi"
linktitle: "get_CssStyleSheetType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType yöntemi. CSS (Cascading Style Sheet) stillerinin HTML, MHTML veya EPUB'a nasıl dışa aktarılacağını belirtir. Varsayılan değer C++'ta HTML/MHTML için Inline, EPUB için External'tur."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheettype/
---
## HtmlSaveOptions::get_CssStyleSheetType method


CSS (Cascading [Style](../../../aspose.words/style/) Sheet) stillerinin HTML, MHTML veya EPUB'a nasıl dışa aktarılacağını belirtir. Varsayılan değer HTML/MHTML için [Inline](../../cssstylesheettype/), EPUB için [External](../../cssstylesheettype/) dir.

```cpp
Aspose::Words::Saving::CssStyleSheetType Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType() const
```

## Açıklamalar


[Saving](../../) CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.

## Ayrıca Bakınız

* Enum [CssStyleSheetType](../../cssstylesheettype/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
