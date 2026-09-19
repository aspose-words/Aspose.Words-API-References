---
title: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings metodo"
linktitle: "LoadWindowsSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings metodo. Carica le impostazioni predefinite di sostituzione delle tabelle per la piattaforma Windows in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule::LoadWindowsSettings method


Carica le impostazioni di sostituzione della tabella predefinite per la piattaforma Windows.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings()
```


## Esempi



Mostra come accedere alle tabelle di sostituzione dei font per Windows e Linux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Crea una nuova regola di sostituzione della tabella e carica la tabella di sostituzione dei font predefinita di Microsoft Windows.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// In Windows, il sostituto predefinito per il font "Times New Roman CE" è "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Possiamo salvare la tabella sotto forma di documento XML.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux ha la sua propria tabella di sostituzione.
// Ci sono più font di sostituzione per "Times New Roman CE".
// Se il primo sostituto, "FreeSerif", è anch'esso non disponibile,
// questa regola ciclerà tra gli altri nell'array finché non ne troverà uno disponibile.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Salva la tabella di sostituzione di Linux sotto forma di documento XML usando uno stream.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## Vedi anche

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
