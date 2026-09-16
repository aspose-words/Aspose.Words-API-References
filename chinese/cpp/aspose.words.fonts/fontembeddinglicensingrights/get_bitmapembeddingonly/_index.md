---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly 方法"
linktitle: "get_BitmapEmbeddingOnly"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly 方法。指示 C++ 中的 “Bitmap embedding only” 限制。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_bitmapembeddingonly/
---
## FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly method


指示“仅位图嵌入”限制。

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly() const
```


## 示例



展示如何获取嵌入字体的许可证权利信息（[FontInfo](../../fontinfo/)）。
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

* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
