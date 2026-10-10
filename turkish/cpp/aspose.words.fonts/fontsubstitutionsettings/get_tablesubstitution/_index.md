---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution metodu"
linktitle: "get_TableSubstitution"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution metodu. C++'de tablo ikame kuralıyla ilgili ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fonts/fontsubstitutionsettings/get_tablesubstitution/
---
## FontSubstitutionSettings::get_TableSubstitution method


[Settings](../../../aspose.words.settings/) related to table substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution() const
```


## Örnekler



Özel yazı tipi değiştirme tablolarıyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Yeni bir tablo değiştirme kuralı oluşturun ve varsayılan Windows yazı tipi değiştirme tablosunu yükleyin.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// Yazı tiplerini yalnızca klasörümüzden seçersek, özel bir değiştirme tablosuna ihtiyacımız olacak.
// Artık Microsoft Windows yazı tiplerine erişemeyeceğiz,
// örneğin "Arial" veya "Times New Roman" çünkü yeni font klasörümüzde mevcut değiller.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Aşağıda yerel dosya sistemindeki bir dosyadan ikame tablosu yüklemenin iki yolu verilmiştir.
// 1 -  Bir akıştan:
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Doğrudan bir dosyadan:
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// "Arial"a artık erişemediğimiz için, font tablomuz önce onu "Nonexistent Font" ile ikame etmeye çalışacak.
// Bu fonta sahip olmadığımız için, "MyFonts" klasöründe bulunan bir sonraki ikame olan "Kreon"a geçecektir.
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// Bu tabloyu programlı olarak genişletebiliriz. "Times New Roman"ı "Arvo" ile ikame eden bir giriş ekleyeceğiz.
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Mevcut bir font girdisi için AddSubstitutes() ile ikincil bir yedek ikame ekleyebiliriz.
// "Arvo" mevcut değilse, tablomuz ikinci ikame seçeneği olarak "M+ 2m"'yi arayacak.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() bir font için yeni ikame fontlar listesi ayarlayabilir.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Erişemediğimiz fontlarla metin yazmak, ikame kurallarımızı devreye sokacaktır.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## Ayrıca Bakınız

* Class [TableSubstitutionRule](../../tablesubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
