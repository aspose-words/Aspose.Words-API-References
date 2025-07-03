---
title: Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType method
linktitle: GetEmbeddedFontAsOpenType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType method. Gets an embedded font file in OpenType format. Fonts in Embedded OpenType format are converted to OpenType in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo::GetEmbeddedFontAsOpenType method


Gets an embedded font file in OpenType format. [Fonts](../../) in Embedded OpenType format are converted to OpenType.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle style)
```


| Parameter | Type | Description |
| --- | --- | --- |
| style | Aspose::Words::Fonts::EmbeddedFontStyle | Specifies the font style to retrieve. |

### ReturnValue

Returns **null** if the specified font is not embedded.

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

* Enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
