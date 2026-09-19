---
title: "Aspose::Words::Fonts::TableSubstitutionRule classe"
linktitle: "TableSubstitutionRule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule classe. Regola di sostituzione dei caratteri della tabella. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


Regola di sostituzione dei caratteri per le tabelle. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Aggiunge nomi di caratteri sostitutivi per il nome del carattere originale fornito. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifica se la regola è abilitata o meno. |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | Restituisce un array contenente i nomi dei caratteri sostitutivi per il nome del carattere originale specificato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | Carica le impostazioni di sostituzione della tabella da un file XML. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | Carica le impostazioni di sostituzione della tabella dallo stream XML. |
| [LoadAndroidSettings](./loadandroidsettings/)() | Carica le impostazioni di sostituzione della tabella predefinite per la piattaforma Android. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | Carica le impostazioni di sostituzione della tabella predefinite per la piattaforma Linux. |
| [LoadWindowsSettings](./loadwindowssettings/)() | Carica le impostazioni di sostituzione della tabella predefinite per la piattaforma Windows. |
| [Save](./save/)(const System::String\&) | Salva le impostazioni di sostituzione della tabella correnti su file. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Salva le impostazioni di sostituzione della tabella correnti su stream. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Impostatore per [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Sovrascrivi i nomi dei font di sostituzione per il nome del font originale fornito. |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
