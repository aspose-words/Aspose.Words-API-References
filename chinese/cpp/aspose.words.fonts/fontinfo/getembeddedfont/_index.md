---
title: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFont method"
linktitle: "GetEmbeddedFont"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFont 方法。获取 C++ 中的特定嵌入字体文件。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo::GetEmbeddedFont method


获取特定的嵌入式字体文件。

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat format, Aspose::Words::Fonts::EmbeddedFontStyle style)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 格式 | Aspose::Words::Fonts::EmbeddedFontFormat | 指定要检索的字体格式。 |
| 样式 | Aspose::Words::Fonts::EmbeddedFontStyle | 指定要检索的字体样式。 |

### ReturnValue

如果指定的字体未嵌入，则返回 **null**。

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

* Enum [EmbeddedFontFormat](../../embeddedfontformat/)
* Enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
