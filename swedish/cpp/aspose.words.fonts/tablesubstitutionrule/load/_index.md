---
title: "Aspose::Words::Fonts::TableSubstitutionRule::Load metod"
linktitle: "Load"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::TableSubstitutionRule::Load metod. Laddar tabellersättningsinställningar från XML‑ström i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fonts/tablesubstitutionrule/load/
---
## TableSubstitutionRule::Load(const System::SharedPtr\<System::IO::Stream\>\&) method


Läser in tabellsubstitutionsinställningar från en XML-ström.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Load(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Indata‑ström. |

## Exempel



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
## TableSubstitutionRule::Load(const System::String\&) method


Läser in tabellsubstitutionsinställningar från en XML-fil.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Load(const System::String &fileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Indatafilnamn. |

## Exempel



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
