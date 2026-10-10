---
title: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings metod"
linktitle: "LoadWindowsSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings metod. Laddar fördefinierade tabellsubstitutionsinställningar för Windows-plattformen i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule::LoadWindowsSettings method


Läser in fördefinierade tabellsubstitutionsinställningar för Windows-plattformen.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings()
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
