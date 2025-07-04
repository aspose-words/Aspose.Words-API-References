---
title: Aspose::Words::Fonts::EmbeddedFontStyle enum
linktitle: EmbeddedFontStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::EmbeddedFontStyle enum. Specifies the style of an embedded font inside a FontInfo object in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Specifies the style of an embedded font inside a [FontInfo](../fontinfo/) object.

```cpp
enum class EmbeddedFontStyle
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Regular | 0 | Specifies the Regular embedded font. |
| Bold | 1 | Specifies the Bold embedded font. |
| Italic | 2 | Specifies the Italic embedded font. |
| BoldItalic | 3 | Specifies the Bold-Italic embedded font. |


## Examples



Shows how to extract an embedded font from a document, and save it to the local file system. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Embedded font formats may be different in other formats such as .doc.
// We need to know the correct format before we can extract the font.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## See Also

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
