---
title: EmbeddedFontFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies format of particular embedded font inside FontInfo object. When saving a document to a file, only embedded fonts of corresponding format are written down.
type: docs
weight: 235
url: /cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Specifies format of particular embedded font inside [FontInfo](../fontinfo/) object. When saving a document to a file, only embedded fonts of corresponding format are written down.

### Values

| Name | Value | Description |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Specifies Embedded OpenType (EOT) File Format. This format of embedded fonts used in DOC files. |
| OpenType | 1 | Specifies font, embedded as plain copy of OpenType (TrueType) font file. This format of embedded fonts used in Open Office XML format, including DOCX files. |


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

