---
title: EmbeddedFontStyle
second_title: Aspose.Words for C++ API Reference
description: Specifies the style of an embedded font inside a FontInfo object.
type: docs
weight: 248
url: /cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Specifies the style of an embedded font inside a [FontInfo](../fontinfo/) object.

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
auto doc = MakeObject<Document>(MyDir + u"Embedded font.docx");

SharedPtr<FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(EmbeddedFontFormat::OpenType, EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(ArtifactsDir + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Embedded font formats may be different in other formats such as .doc.
// We need to know the correct format before we can extract the font.
doc = MakeObject<Document>(MyDir + u"Embedded font.doc");

ASSERT_TRUE(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(EmbeddedFontFormat::OpenType, EmbeddedFontStyle::Regular) ==
            nullptr);
ASSERT_FALSE(
    doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(EmbeddedFontFormat::EmbeddedOpenType, EmbeddedFontStyle::Regular) ==
    nullptr);

// Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(ArtifactsDir + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

