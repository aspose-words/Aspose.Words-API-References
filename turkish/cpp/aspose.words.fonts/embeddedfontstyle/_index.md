---
title: "Aspose::Words::Fonts::EmbeddedFontStyle enum"
linktitle: "EmbeddedFontStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::EmbeddedFontStyle enum. C++'de bir FontInfo nesnesi içindeki gömülü fontun stilini belirtir."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Bir [FontInfo](../fontinfo/) nesnesi içindeki gömülü fontun stilini belirtir.

```cpp
enum class EmbeddedFontStyle
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Regular | 0 | Düzenli gömülü yazı tipini belirtir. |
| Kalın | 1 | Kalın gömülü yazı tipini belirtir. |
| İtalik | 2 | İtalik gömülü yazı tipini belirtir. |
| Kalınİtalik | 3 | Kalın-İtalik gömülü yazı tipini belirtir. |


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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
