---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType"
linktitle: "get_CssStyleSheetType"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType. Указывает, как стили CSS (Cascading Style Sheet) экспортируются в HTML, MHTML или EPUB. Значение по умолчанию — Inline для HTML/MHTML и External для EPUB в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheettype/
---
## HtmlSaveOptions::get_CssStyleSheetType method


Указывает, как стили CSS (Cascading [Style](../../../aspose.words/style/) Sheet) экспортируются в HTML, MHTML или EPUB. Значение по умолчанию — [Inline](../../cssstylesheettype/) для HTML/MHTML и [External](../../cssstylesheettype/) для EPUB.

```cpp
Aspose::Words::Saving::CssStyleSheetType Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType() const
```

## Примечания


[Saving](../../) CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.

## См. также

* Enum [CssStyleSheetType](../../cssstylesheettype/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
