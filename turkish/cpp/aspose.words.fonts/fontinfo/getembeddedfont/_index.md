---
title: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFont metodu"
linktitle: "GetEmbeddedFont"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFont metodu. C++'da belirli bir gömülü yazı tipi dosyası alır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo::GetEmbeddedFont method


Belirli bir gömülü yazı tipi dosyasını alır.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat format, Aspose::Words::Fonts::EmbeddedFontStyle style)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| biçim | Aspose::Words::Fonts::EmbeddedFontFormat | Alınacak yazı tipi biçimini belirtir. |
| stil | Aspose::Words::Fonts::EmbeddedFontStyle | Alınacak yazı tipi stilini belirtir. |

### ReturnValue

Belirtilen yazı tipi gömülü değilse **null** döndürür.

## Örnekler



Bir belgeden gömülü bir yazı tipinin nasıl çıkarılacağını ve yerel dosya sistemine nasıl kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Gömülü yazı tipi biçimleri, .doc gibi diğer biçimlerde farklı olabilir.
// Yazı tipini çıkarabilmek için doğru biçimi bilmemiz gerekir.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// Ayrıca, .doc belgelerinden gelen gömülü OpenType biçimini OpenType’a dönüştürebiliriz.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## Ayrıca Bakınız

* Enum [EmbeddedFontFormat](../../embeddedfontformat/)
* Enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
