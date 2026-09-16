---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method"
linktitle: "get_CssStyleSheetFileName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName 方法。指定在将文档导出为 HTML 时写入的层叠样式表（CSS）文件的路径和名称。默认在 C++ 中为空字符串。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


指定在将文档导出为 HTML 时写入的层叠 [Style](../../../aspose.words/style/) 表（CSS）文件的路径和名称。默认为空字符串。

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## 备注


此属性仅在将文档保存为 HTML 格式且使用 [CssStyleSheetType](../get_cssstylesheettype/) 请求外部 CSS 样式表时生效。

如果此属性为空，CSS 文件将保存到与 HTML 文档相同的文件夹，并使用相同的文件名，但扩展名为 ".css"。

如果此属性仅指定了路径而未指定文件名，CSS 文件将保存到指定的文件夹，并使用与 HTML 文档相同的文件名，但扩展名为 ".css"。

如果此属性指定的文件夹不存在，它将在保存 CSS 文件之前自动创建。

指定外部 CSS 文件保存位置的另一种方式是使用 [ResourceFolder](../get_resourcefolder/)。

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
