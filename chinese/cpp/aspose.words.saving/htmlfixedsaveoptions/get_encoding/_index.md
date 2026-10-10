---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding 方法"
linktitle: "get_Encoding"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding 方法。指定导出为 HTML 时使用的编码。默认值在 C++ 中为 new UTF8Encoding(true)（带 BOM 的 UTF-8）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


指定导出为 HTML 时使用的编码。默认值为 **new UTF8Encoding(true)**（带 BOM 的 UTF-8）。

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## 示例



展示如何设置在导出文档为 HTML 时使用的编码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// 默认编码是 UTF-8。如果我们想使用不同的编码来表示文档，
// 我们可以使用 SaveOptions 对象来设置特定的编码。
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
