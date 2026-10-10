---
title: "Aspose::Words::Fonts::TableSubstitutionRule::Save metodo"
linktitle: "Save"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule::Save metodo. Salva le impostazioni correnti di sostituzione delle tabelle nello stream in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.fonts/tablesubstitutionrule/save/
---
## TableSubstitutionRule::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Salva le impostazioni di sostituzione della tabella correnti su stream.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Stream di output. |

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
## TableSubstitutionRule::Save(const System::String\&) method


Salva le impostazioni di sostituzione della tabella correnti su file.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Save(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Nome file di output. |

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
