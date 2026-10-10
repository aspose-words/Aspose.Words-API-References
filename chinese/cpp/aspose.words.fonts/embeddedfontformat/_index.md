---
title: "Aspose::Words::Fonts::EmbeddedFontFormat 枚举"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::EmbeddedFontFormat enum. 指定 FontInfo 对象中特定嵌入字体的格式。将文档保存为文件时，仅会写入对应格式的嵌入字体（C++）。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


指定 [FontInfo](../fontinfo/) 对象中特定嵌入字体的格式。将文档保存为文件时，仅会写入对应格式的嵌入字体。

```cpp
enum class EmbeddedFontFormat
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| EmbeddedOpenType | 0 | 指定 Embedded OpenType (EOT) 文件格式。此嵌入字体格式用于 DOC 文件。 |
| OpenType | 1 | 指定字体，以 OpenType (TrueType) 字体文件的纯拷贝形式嵌入。此嵌入字体格式用于 Open Office XML 格式，包括 DOCX 文件。 |


## 示例



展示如何从文档中提取嵌入字体并将其保存到本地文件系统。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// 嵌入字体的格式在其他格式（如 .doc）中可能不同。
// 我们需要先了解正确的格式才能提取字体。
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// 此外，我们可以将来自 .doc 文档的嵌入 OpenType 格式转换为 OpenType。
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## 另见

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
