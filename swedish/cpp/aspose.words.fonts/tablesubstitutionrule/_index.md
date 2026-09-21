---
title: "Aspose::Words::Fonts::TableSubstitutionRule klass"
linktitle: "TableSubstitutionRule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::TableSubstitutionRule klass. Regel för teckensnittssubstitution i tabell. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


Tabellteckensnittssubstitutionsregel. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Lägger till ersättande teckensnittsnamn för ett givet originalteckensnittsnamn. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Anger om regeln är aktiverad eller inte. |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | Returnerar en array som innehåller ersättande teckensnittsnamn för det angivna originalteckensnittsnamnet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | Läser in tabellsubstitutionsinställningar från en XML-fil. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | Läser in tabellsubstitutionsinställningar från en XML-ström. |
| [LoadAndroidSettings](./loadandroidsettings/)() | Läser in fördefinierade tabellsubstitutionsinställningar för Android-plattformen. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | Läser in fördefinierade tabellsubstitutionsinställningar för Linux-plattformen. |
| [LoadWindowsSettings](./loadwindowssettings/)() | Läser in fördefinierade tabellsubstitutionsinställningar för Windows-plattformen. |
| [Save](./save/)(const System::String\&) | Sparar de aktuella tabellsubstitutionsinställningarna till en fil. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Sparar de aktuella tabellsubstitutionsinställningarna till en ström. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Sättare för [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Åsidosätt ersättande teckensnittsnamn för ett givet originalteckensnittsnamn. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man får åtkomst till teckensnittssubstitutionstabeller för Windows och Linux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Skapa en ny tabellsubstitutionsregel och läs in standardtabellen för teckensnittssubstitution i Microsoft Windows.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// I Windows är standardersättningen för teckensnittet "Times New Roman CE" "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Vi kan spara tabellen i form av ett XML-dokument.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux har sin egen substitutionstabell.
// Det finns flera ersättande teckensnitt för "Times New Roman CE".
// Om den första ersättningen, "FreeSerif", också är otillgänglig,
// kommer den här regeln att cykla igenom de andra i arrayen tills den hittar en som är tillgänglig.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Spara Linux‑substitutionstabellen i form av ett XML-dokument med en ström.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## Se även

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
