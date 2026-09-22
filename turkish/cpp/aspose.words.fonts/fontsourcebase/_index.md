---
title: "Aspose::Words::Fonts::FontSourceBase sınıfı"
linktitle: "FontSourceBase"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSourceBase sınıfı. Kullanıcının çeşitli yazı tipi kaynaklarını belirtmesine izin veren sınıflar için soyut bir temel sınıftır. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


Bu, kullanıcının çeşitli yazı tipi kaynaklarını belirtmesine izin veren sınıflar için soyut bir temel sınıftır. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FontSourceBase : public Aspose::Fonts::IFontSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Priority](./get_priority/)() const | Yazı tipi kaynağı önceliğini döndürür. |
| virtual [get_Type](./get_type/)() | Yazı tipi kaynağının türünü döndürür. |
| [get_WarningCallback](./get_warningcallback/)() const | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| [GetAvailableFonts](./getavailablefonts/)() | Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
