---
title: "Aspose::Words::Fonts::EmbeddedFontStyle 枚举"
linktitle: "EmbeddedFontStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::EmbeddedFontStyle 枚举。指定 C++ 中 FontInfo 对象内嵌入字体的样式。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


指定嵌入字体在 [FontInfo](../fontinfo/) 对象中的样式。

```cpp
enum class EmbeddedFontStyle
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Regular | 0 | 指定 Regular 嵌入字体。 |
| 粗体 | 1 | 指定粗体嵌入字体。 |
| 斜体 | 2 | 指定斜体嵌入字体。 |
| 粗斜体 | 3 | 指定粗斜体嵌入字体。 |


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
