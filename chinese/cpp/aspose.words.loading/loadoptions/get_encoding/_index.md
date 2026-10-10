---
title: "Aspose::Words::Loading::LoadOptions::get_Encoding 方法"
linktitle: "get_Encoding"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_Encoding 方法。获取或设置在文档内部未指定编码时用于加载 HTML、TXT 或 CHM 文档的编码。可以为 null。默认在 C++ 中为 null。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


获取或设置在文档内部未指定编码时用于加载 HTML、TXT 或 CHM 文档的编码。可以为 **null**。默认值为 **null**。

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## 备注


此属性仅在加载 HTML、TXT 或 CHM 文档时使用。

如果文档内部未指定编码且此属性为 **null**，系统将尝试自动检测编码。

## 示例



展示如何设置打开文档时使用的编码。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// 在传入 LoadOptions 对象的同时加载文档，然后验证文档的内容。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## 另见

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
