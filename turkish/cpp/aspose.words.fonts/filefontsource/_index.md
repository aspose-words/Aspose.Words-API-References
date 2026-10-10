---
title: "Aspose::Words::Fonts::FileFontSource class"
linktitle: "FileFontSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FileFontSource sınıfı. Dosya sisteminde depolanan tek bir TrueType yazı tipi dosyasını temsil eder. Daha fazla bilgi için C++'daki  dokümantasyon makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


Dosya sisteminde depolanan tek TrueType yazı tipi dosyasını temsil eder. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | Yapıcı. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | Yapıcı. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | Yapıcı. |
| [get_CacheKey](./get_cachekey/)() const | Bu kaynağın önbellekteki anahtarı. |
| [get_FilePath](./get_filepath/)() const | Yazı tipi dosyasının yolu. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Yazı tipi kaynağı önceliğini döndürür. |
| [get_Type](./get_type/)() override | Yazı tipi kaynağının türünü döndürür. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| static [Type](./type/)() |  |

## Örnekler



Yerel dosya sistemindeki bir yazı tipi dosyasını yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Ayrıca Bakınız

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
