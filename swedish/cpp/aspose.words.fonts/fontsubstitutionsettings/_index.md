---
title: "Aspose::Words::Fonts::FontSubstitutionSettings klass"
linktitle: "FontSubstitutionSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontSubstitutionSettings klass. Anger inställningar för teckensnittssubstitutionsmekanismen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class


Specificerar inställningar för teckensnittssubstitutionsmekanismen. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionSettings : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DefaultFontSubstitution](./get_defaultfontsubstitution/)() const | [Settings](../../aspose.words.settings/) relaterade till standardteckensnittssubstitutionsregeln. |
| [get_FontConfigSubstitution](./get_fontconfigsubstitution/)() const | [Settings](../../aspose.words.settings/) relaterade till teckensnittskonfigurationssubstitutionsregeln. |
| [get_FontInfoSubstitution](./get_fontinfosubstitution/)() const | [Settings](../../aspose.words.settings/) relaterade till teckensnittsinformationssubstitutionsregeln. |
| [get_FontNameSubstitution](./get_fontnamesubstitution/)() const | [Settings](../../aspose.words.settings/) relaterade till teckensnittsnamnssubstitutionsregeln. |
| [get_TableSubstitution](./get_tablesubstitution/)() const | [Settings](../../aspose.words.settings/) relaterade till tabellsubstitutionsregeln. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Anmärkningar


[Font](../../aspose.words/font/) substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

Regelordningen är följande:1. [Font](../../aspose.words/font/) namnsubstitutionsregeln (aktiverad som standard)
1. [Font](../../aspose.words/font/) konfigurationssubstitutionsregeln (inaktiverad som standard)
1. Tabellsubstitutionsregeln (aktiverad som standard)
1. [Font](../../aspose.words/font/) info-ersättningsregel (aktiverad som standard)
1. Standardteckensnittregel (aktiverad som standard)



Observera att font-info-ersättningsregeln alltid kommer att lösa teckensnittet om [FontInfo](../fontinfo/) är tillgänglig och kommer att åsidosätta standardteckensnittregeln. Om du vill använda standardteckensnittregeln bör du inaktivera font-info-ersättningsregeln.

Observera att font-konfigurations-ersättningsregeln kommer att lösa teckensnittet i de flesta fall och därmed åsidosätter alla andra regler.

## Exempel



Visar hur man får åtkomst till ett dokuments systemteckensnittskälla och ställer in teckensnittssubstitut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Som standard innehåller ett tomt dokument alltid en systemteckensnittskälla.
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

// Ställ in ett teckensnitt som finns i Windows Fonts-katalogen som ersättning för ett som inte finns.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// Alternativt kan vi lägga till en mappteckensnittskälla där den motsvarande mappen innehåller teckensnittet.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// Att återställa teckensnittskällorna lämnar fortfarande kvar systemets teckensnittskälla samt våra ersättningar.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```

## Se även

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
