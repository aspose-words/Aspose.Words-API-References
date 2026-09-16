---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions 枚举"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions 枚举。表示 C++ 中字体嵌入使用权限。"
type: docs
weight: 20500
url: /zh/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


表示字体嵌入的使用权限。

```cpp
enum class FontEmbeddingUsagePermissions
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Installable | 0 | 该字体可以嵌入，并且可以永久安装，以供远程系统或其他用户使用。 |
| RestrictedLicense | 1 | 未经合法所有者明确许可，禁止以任何方式修改、嵌入或交换该字体。 |
| PrintAndPreview | 2 | 该字体可以嵌入，并可临时加载到其他系统，以用于文档的查看或打印。 |
| Editable | 3 | 该字体可以嵌入，并可临时加载到其他系统。 |


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
