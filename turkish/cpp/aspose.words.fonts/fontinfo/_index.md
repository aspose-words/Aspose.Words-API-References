---
title: "Aspose::Words::Fonts::FontInfo sınıfı"
linktitle: "FontInfo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfo sınıfı. Belgede kullanılan bir yazı tipi hakkında bilgi belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


Belgede kullanılan bir yazı tipi hakkında bilgileri belirtir. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FontInfo : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AltName](./get_altname/)() const | Yazı tipinin alternatif adını alır veya ayarlar. |
| [get_Charset](./get_charset/)() | Yazı tipinin karakter kümesini alır veya ayarlar. |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | Gömülü yazı tipi lisans haklarını alır. |
| [get_Family](./get_family/)() const | Bu yazı tipinin ait olduğu yazı tipi ailesini alır veya ayarlar. |
| [get_IsTrueType](./get_istruetype/)() const | Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu gösterir. Varsayılan **true**. |
| [get_Name](./get_name/)() const | Yazı tipinin adını alır. |
| [get_Panose](./get_panose/)() const | PANOSE yazı tipi sınıflandırma numarasını alır veya ayarlar. |
| [get_Pitch](./get_pitch/)() const | Pitch, yazı tipinin sabit pitch, orantılı aralıklı olup olmadığını veya varsayılan bir ayara dayanıp dayanmadığını gösterir. |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | Belirli bir gömülü yazı tipi dosyasını alır. |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | OpenType formatında bir gömülü yazı tipi dosyasını alır. Embedded OpenType formatındaki [Fonts](../) OpenType'a dönüştürülür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/). |
| [set_Charset](./set_charset/)(int32_t) | Ayarlayıcı [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/). |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | Ayarlayıcı [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/). |
| [set_IsTrueType](./set_istruetype/)(bool) | Ayarlayıcı [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/). |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | Ayarlayıcı [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/). |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | Ayarlayıcı [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/). |
| static [Type](./type/)() |  |
## Açıklamalar


Bu sınıfın örneklerini doğrudan oluşturmazsınız. Bir belgede tanımlı yazı tipleri koleksiyonuna erişmek için [FontInfos](../../aspose.words/documentbase/get_fontinfos/) özelliğini kullanın.

## Örnekler



Bir belgede mevcut olan yazı tiplerinin ayrıntılarını nasıl yazdıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Belgedeki kullanılan ve kullanılmayan tüm yazı tiplerini yazdırın.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
