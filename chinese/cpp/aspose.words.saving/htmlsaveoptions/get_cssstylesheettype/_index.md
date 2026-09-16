---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType 方法"
linktitle: "get_CssStyleSheetType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType 方法。指定 CSS（层叠样式表）样式如何导出为 HTML、MHTML 或 EPUB。在 C++ 中，默认值为 HTML/MHTML 的 Inline 和 EPUB 的 External。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheettype/
---
## HtmlSaveOptions::get_CssStyleSheetType method


指定 CSS（层叠 [Style](../../../aspose.words/style/) Sheet）样式如何导出为 HTML、MHTML 或 EPUB。默认值为 HTML/MHTML 的 [Inline](../../cssstylesheettype/) 和 EPUB 的 [External](../../cssstylesheettype/)。

```cpp
Aspose::Words::Saving::CssStyleSheetType Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType() const
```

## 备注


[Saving](../../) CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.

## 另见

* Enum [CssStyleSheetType](../../cssstylesheettype/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
