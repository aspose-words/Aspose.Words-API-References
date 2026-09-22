---
title: "Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes yöntemi"
linktitle: "SetSubstitutes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes yöntemi. C++'ta verilen özgün yazı tipi adı için yedek yazı tipi adlarını geçersiz kılar."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule::SetSubstitutes method


Belirtilen orijinal yazı tipi adı için ikame yazı tipi adlarını geçersiz kılar.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| originalFontName | const System::String\& | Özgün yazı tipi adı. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | Alternatif yazı tipi adlarının listesi. |

## Örnekler



Yazı tipi değiştirme kurallarının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Varsayılan yazı tipi kaynakları, belgenin kullandığı ilk yazı tipini içerir.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// İkinci yazı tipi, "Amethysta", mevcut değil.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Yazı tipi değiştirme tablosunu yapılandırabiliriz, bu tablo belirler
// hangi yazı tiplerinin Aspose.Words tarafından mevcut olmayan yazı tipleri için yedek olarak kullanılacağını.
// "Amethysta" için iki yedek yazı tipi ayarlayın: "Arvo" ve "Courier New".
// İlk yedek mevcut değilse, Aspose.Words ikinci yedeği kullanmayı dener ve bu şekilde devam eder.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" mevcut değil ve değiştirme kuralı, yedek olarak kullanılacak ilk yazı tipinin "Arvo" olduğunu belirtir.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" da mevcut değil, ancak "Courier New" mevcut.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Çıktı belgesi, "Amethysta" yazı tipini kullanan metni "Courier New" ile biçimlendirilmiş olarak gösterecek.
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
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
