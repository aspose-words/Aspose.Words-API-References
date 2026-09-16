---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow 方法"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow 方法。获取或设置一个值，以确定在 C++ 中输出的 Pdf 文档中的超链接是否被强制在浏览器的新窗口（或标签页）中打开。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


获取或设置一个值，以确定输出 Pdf 文档中的超链接是否强制在浏览器的新窗口（或标签页）中打开。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## 备注


默认值为 **false**。当此值设置为 **true** 时，超链接将使用 JavaScript 代码保存。JavaScript 代码为 **app.launchURL(\"URL\", true);**，其中 **URL** 是一个超链接。

请注意，如果此选项设置为 **true**，超链接可能无法在某些 PDF 阅读器中工作，例如 Chrome、Firefox。

PDF/A-1、PDF/A-2 和 PDF/A-3 合规性禁止 JavaScript 动作。在这种情况下将自动使用 **false** 值。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
