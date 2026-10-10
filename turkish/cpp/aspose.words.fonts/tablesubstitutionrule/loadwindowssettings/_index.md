---
title: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings yöntemi"
linktitle: "LoadWindowsSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings yöntemi. Windows platformu için önceden tanımlı tablo ikame ayarlarını C++'da yükler."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule::LoadWindowsSettings method


Windows platformu için önceden tanımlı tablo ikame ayarlarını yükler.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings()
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
