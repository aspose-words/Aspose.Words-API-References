---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins 方法"
linktitle: "get_PageMargins"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins 方法。指定 HTML 文档中页面周围的边距。边距值以点为单位，且应大于或等于 0。默认值在 C++ 中为 10 点。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagemargins/
---
## HtmlFixedSaveOptions::get_PageMargins method


指定 HTML 文档中页面的边距。边距值以点为单位，且应大于或等于 0。默认值为 10 点。

```cpp
double Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins() const
```

## 备注


取决于 [PageHorizontalAlignment](../get_pagehorizontalalignment/) 属性的值：

* Defines top, bottom and left page margins if the value is [Left](../../htmlfixedpagehorizontalalignment/).
* Defines top, bottom and right page margins if the value is [Right](../../htmlfixedpagehorizontalalignment/).
* Defines top and bottom page margins if the value is [Center](../../htmlfixedpagehorizontalalignment/).



## 示例



展示如何在将文档保存为 HTML 时调整页面边距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_PageMargins(15);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")->get_Success());
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
