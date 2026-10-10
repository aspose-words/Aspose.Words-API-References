---
title: "Aspose::Words::Fonts::TableSubstitutionRule::AddSubstitutes metod"
linktitle: "AddSubstitutes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::TableSubstitutionRule::AddSubstitutes metod. Lägger till ersättnings-typsnittsnamn för ett givet originaltypsnittsnamn i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fonts/tablesubstitutionrule/addsubstitutes/
---
## TableSubstitutionRule::AddSubstitutes method


Lägger till ersättande teckensnittsnamn för ett givet originalteckensnittsnamn.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::AddSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| originalFontName | const System::String\& | Originalt typsnittnamn. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | Lista över alternativa typsnittnamn. |

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


Visar hur man arbetar med anpassade typsnittsersättningstabeller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Skapa en ny tabellersättningsregel och läs in standard‑Windows‑typsnittsersättningstabellen.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// Om vi väljer typsnitt uteslutande från vår mapp kommer vi att behöva en anpassad ersättningstabell.
// Vi kommer inte längre ha tillgång till Microsoft Windows‑typsnitten,
// såsom \"Arial\" eller \"Times New Roman\" eftersom de inte finns i vår nya typsnittsmapp.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Nedan följer två sätt att läsa in en ersättningstabell från en fil i det lokala filsystemet.
// 1 -  Från en ström:
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Direkt från en fil:
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// Eftersom vi inte längre har åtkomst till "Arial" kommer vår teckensnittstabell först att försöka ersätta den med "Nonexistent Font".
// Vi har inte detta teckensnitt så den kommer att gå vidare till nästa ersättning, "Kreon", som finns i mappen "MyFonts".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// Vi kan expandera den här tabellen programmässigt. Vi kommer att lägga till en post som ersätter "Times New Roman" med "Arvo"
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Vi kan lägga till ett sekundärt reserversättningsalternativ för en befintlig teckensnittspost med AddSubstitutes().
// Om "Arvo" inte är tillgängligt kommer vår tabell att leta efter "M+ 2m" som ett andra ersättningsalternativ.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() kan ange en ny lista med ersättningsteckensnitt för ett teckensnitt.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Att skriva text i teckensnitt som vi inte har åtkomst till kommer att utlösa våra ersättningsregler.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## Se även

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
