---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights 类"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights 类。表示在 C++ 中对字体的嵌入许可权。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


表示字体的嵌入许可权。

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | 指示“仅位图嵌入”限制。 |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | 使用权限。 |
| [get_NoSubsetting](./get_nosubsetting/)() const | 指示“无子集化”限制。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 示例



展示如何获取嵌入字体的许可证权利信息（[FontInfo](../fontinfo/)）。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// 获取文档字体列表。
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
for (auto&& fontInfo : fontInfos)
{
    if (fontInfo->get_EmbeddingLicensingRights() != nullptr)
    {
        std::cout << System::EnumGetName(fontInfo->get_EmbeddingLicensingRights()->get_EmbeddingUsagePermissions()) << std::endl;
        std::cout << System::Convert::ToString(fontInfo->get_EmbeddingLicensingRights()->get_BitmapEmbeddingOnly()) << std::endl;
        std::cout << System::Convert::ToString(fontInfo->get_EmbeddingLicensingRights()->get_NoSubsetting()) << std::endl;
    }
}
```

## 另见

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
