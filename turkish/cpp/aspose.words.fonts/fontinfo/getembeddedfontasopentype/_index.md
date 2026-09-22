---
title: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType metodu"
linktitle: "GetEmbeddedFontAsOpenType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType metodu. OpenType formatında gömülü bir yazı tipi dosyası alır. Gömülü OpenType formatındaki yazı tipleri C++'da OpenType'a dönüştürülür."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo::GetEmbeddedFontAsOpenType method


OpenType formatında gömülü bir yazı tipi dosyası alır. Gömülü OpenType formatındaki [Yazı tipleri](../../) OpenType'a dönüştürülür.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle style)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
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

* Enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
