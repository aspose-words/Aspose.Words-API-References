---
title: "Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes metodu"
linktitle: "GetSubstitutes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes metodu. C++'ta belirtilen orijinal font adı için ikame font adlarını içeren bir dizi döndürür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fonts/tablesubstitutionrule/getsubstitutes/
---
## TableSubstitutionRule::GetSubstitutes method


Belirtilen orijinal yazı tipi adı için ikame yazı tipi adlarını içeren bir dizi döndürür.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerable<System::String>> Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes(const System::String &originalFontName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| originalFontName | const System::String\& | Özgün yazı tipi adı. |

### ReturnValue

Alternatif yazı tipi adlarının listesi.

## Örnekler



Bir belgenin sistem yazı tipi kaynağına nasıl erişileceğini ve yazı tipi ikamelerini nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Varsayılan olarak, boş bir belge her zaman bir sistem yazı tipi kaynağı içerir.
ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());

auto systemFontSource = System::ExplicitCast<Aspose::Words::Fonts::SystemFontSource>(doc->get_FontSettings()->GetFontsSources()->idx_get(0));
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, systemFontSource->get_Type());
ASSERT_EQ(0, systemFontSource->get_Priority());

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) || (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const System::String fontsPath = u"C:\\WINDOWS\\Fonts";
    System::String actual = System::Default<System::String>();
    System::String condExpression = Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders()->LINQ_FirstOrDefault();
    if (condExpression != nullptr)
    {
        actual = condExpression.ToLower();
    }
    ASSERT_EQ(fontsPath.ToLower(), actual);
}

for (System::String systemFontFolder : Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// Windows Yazı Tipleri dizininde mevcut olan bir yazı tipini, mevcut olmayan bir yazı tipinin ikamesi olarak ayarlayın.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// Alternatif olarak, ilgili klasörün yazı tipini içerdiği bir klasör yazı tipi kaynağı ekleyebiliriz.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// Yazı tipi kaynaklarını sıfırlamak, hâlâ sistem yazı tipi kaynağını ve ikamelerimizi bırakır.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
