---
title: "Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights method"
linktitle: "get_EmbeddingLicensingRights"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights 方法。获取 C++ 中嵌入字体的许可权利。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words.fonts/fontinfo/get_embeddinglicensingrights/
---
## FontInfo::get_EmbeddingLicensingRights method


获取嵌入字体的许可权利。

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights()
```

## 备注


如果字体未嵌入，则该值可能为 null。

## 示例



展示如何获取嵌入字体的许可权利信息（[FontInfo](../)）。
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

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
