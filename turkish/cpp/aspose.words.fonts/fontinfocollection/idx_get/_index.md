---
title: "Aspose::Words::Fonts::FontInfoCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfoCollection::idx_get yöntemi. Belirtilen ada sahip bir yazı tipini C++'ta alır."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.fonts/fontinfocollection/idx_get/
---
## FontInfoCollection::idx_get(const System::String\&) method


Belirtilen isimde bir yazı tipini alır.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfo> Aspose::Words::Fonts::FontInfoCollection::idx_get(const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Bulunacak yazı tipinin büyük/küçük harfe duyarsız adı. |

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

* Class [FontInfo](../../fontinfo/)
* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontInfoCollection::idx_get(int32_t) method


Belirtilen indeksteki bir yazı tipini alır.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfo> Aspose::Words::Fonts::FontInfoCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Yazı tipinin sıfır tabanlı indeksi. |

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

* Class [FontInfo](../../fontinfo/)
* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
