---
title: "Aspose::Words::Fonts::FontSubstitutionSettings class"
linktitle: "FontSubstitutionSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSubstitutionSettings sınıfı. Font ikame mekanizması ayarlarını belirtir. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class


Yazı tipi ikame mekanizması ayarlarını belirtir. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FontSubstitutionSettings : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DefaultFontSubstitution](./get_defaultfontsubstitution/)() const | [Settings](../../aspose.words.settings/) varsayılan font ikame kuralıyla ilgili. |
| [get_FontConfigSubstitution](./get_fontconfigsubstitution/)() const | [Settings](../../aspose.words.settings/) font yapılandırma ikame kuralıyla ilgili. |
| [get_FontInfoSubstitution](./get_fontinfosubstitution/)() const | [Settings](../../aspose.words.settings/) font bilgisi ikame kuralıyla ilgili. |
| [get_FontNameSubstitution](./get_fontnamesubstitution/)() const | [Settings](../../aspose.words.settings/) font adı ikame kuralıyla ilgili. |
| [get_TableSubstitution](./get_tablesubstitution/)() const | [Settings](../../aspose.words.settings/) tablo ikame kuralıyla ilgili. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Açıklamalar


[Font](../../aspose.words/font/) substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

Kuralların sırası aşağıdaki gibidir:1. [Font](../../aspose.words/font/) adı ikame kuralı (varsayılan olarak etkin)
1. [Font](../../aspose.words/font/) yapılandırma ikame kuralı (varsayılan olarak devre dışı)
1. Tablo ikame kuralı (varsayılan olarak etkin)
1. [Font](../../aspose.words/font/) bilgi ikame kuralı (varsayılan olarak etkin)
1. Varsayılan font kuralı (varsayılan olarak etkin)



Font bilgi ikame kuralının, [FontInfo](../fontinfo/) mevcut olduğunda her zaman fontu çözeceğini ve varsayılan font kuralını geçersiz kılacağını unutmayın. Varsayılan font kuralını kullanmak istiyorsanız font bilgi ikame kuralını devre dışı bırakmalısınız.

Font yapılandırma ikame kuralının çoğu durumda fontu çözeceğini ve böylece diğer tüm kuralları geçersiz kıldığını unutmayın.

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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
