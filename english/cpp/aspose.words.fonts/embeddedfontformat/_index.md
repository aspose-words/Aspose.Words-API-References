---
title: Aspose::Words::Fonts::EmbeddedFontFormat enum
linktitle: EmbeddedFontFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::EmbeddedFontFormat enum. Specifies format of particular embedded font inside FontInfo object. When saving a document to a file, only embedded fonts of corresponding format are written down in C++.'
type: docs
weight: 19000
url: /cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Specifies format of particular embedded font inside [FontInfo](../fontinfo/) object. When saving a document to a file, only embedded fonts of corresponding format are written down.

```cpp
enum class EmbeddedFontFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Specifies Embedded OpenType (EOT) File Format. This format of embedded fonts used in DOC files. |
| OpenType | 1 | Specifies font, embedded as plain copy of OpenType (TrueType) font file. This format of embedded fonts used in Open Office XML format, including DOCX files. |


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
