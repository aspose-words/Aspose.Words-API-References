---
title: "Aspose::Words::Fonts::TableSubstitutionRule sınıfı"
linktitle: "TableSubstitutionRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::TableSubstitutionRule sınıfı. Tablo yazı tipi ikame kuralı. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


Tablo yazı tipi ikame kuralı. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Verilen orijinal yazı tipi adı için ikame yazı tipi adları ekler. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Kuralın etkin olup olmadığını belirtir. |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | Belirtilen orijinal yazı tipi adı için ikame yazı tipi adlarını içeren bir dizi döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | XML dosyasından tablo ikame ayarlarını yükler. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | XML akışından tablo ikame ayarlarını yükler. |
| [LoadAndroidSettings](./loadandroidsettings/)() | Android platformu için önceden tanımlı tablo ikame ayarlarını yükler. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | Linux platformu için önceden tanımlı tablo ikame ayarlarını yükler. |
| [LoadWindowsSettings](./loadwindowssettings/)() | Windows platformu için önceden tanımlı tablo ikame ayarlarını yükler. |
| [Save](./save/)(const System::String\&) | Mevcut tablo ikame ayarlarını dosyaya kaydeder. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Mevcut tablo ikame ayarlarını akışa kaydeder. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Ayarlayıcı [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Belirtilen orijinal yazı tipi adı için ikame yazı tipi adlarını geçersiz kılar. |
| static [Type](./type/)() |  |

## Örnekler



Windows ve Linux için yazı tipi ikame tablolarına nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Yeni bir tablo ikame kuralı oluşturur ve varsayılan Microsoft Windows yazı tipi ikame tablosunu yükler.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// Windows'ta, "Times New Roman CE" yazı tipi için varsayılan ikame "Times New Roman"dır.
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Tabloyu bir XML belgesi biçiminde kaydedebiliriz.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux'un kendi ikame tablosu vardır.
// "Times New Roman CE" için birden fazla ikame yazı tipi vardır.
// İlk ikame, "FreeSerif" de mevcut değilse,
// bu kural, mevcut bir tane bulana kadar dizideki diğerlerine dönecektir.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Linux ikame tablosunu bir akış kullanarak XML belgesi biçiminde kaydedin.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## Ayrıca Bakınız

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
