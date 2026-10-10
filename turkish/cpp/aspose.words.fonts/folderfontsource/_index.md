---
title: "Aspose::Words::Fonts::FolderFontSource sınıfı"
linktitle: "FolderFontSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FolderFontSource sınıfı. TrueType yazı tipi dosyalarını içeren klasörü temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


TrueType yazı tipi dosyalarını içeren klasörü temsil eder. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | Yapıcı. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | Yapıcı. |
| [get_FolderPath](./get_folderpath/)() const | Klasörün yolu. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Yazı tipi kaynağı önceliğini döndürür. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | Alt klasörlerin taranıp taranmayacağını belirler. |
| [get_Type](./get_type/)() override | Yazı tipi kaynağının türünü döndürür. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| static [Type](./type/)() |  |

## Örnekler



Yazı tipi kaynağı olarak yazı tiplerini içeren yerel bir sistem klasörünün nasıl kullanılacağını gösterir.
```cpp
// Yazı tipi dosyalarını içeren bir klasörden yazı tipi kaynağı oluştur.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Ayrıca Bakınız

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
