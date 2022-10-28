---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Gets a font with the specified name.
type: docs
weight: 131
url: /cpp/aspose.words.fonts/fontinfocollection/idx_get/
---
## FontInfoCollection.idx_get(const System::String\&) method


Gets a font with the specified name.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfo> Aspose::Words::Fonts::FontInfoCollection::idx_get(const System::String &name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Case-insensitive name of the font to locate. |

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

## FontInfoCollection.idx_get(int32_t) method


Gets a font at the specified index.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfo> Aspose::Words::Fonts::FontInfoCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | Zero-based index of the font. |

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

