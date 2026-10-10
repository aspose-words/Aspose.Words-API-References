---
title: "Aspose::Words::Fonts::TableSubstitutionRule::LoadLinuxSettings method"
linktitle: "LoadLinuxSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::TableSubstitutionRule::LoadLinuxSettings method. Lädt vordefinierte Tabellenersetzungseinstellungen für die Linux-Plattform in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/
---
## TableSubstitutionRule::LoadLinuxSettings method


Lädt vordefinierte Tabellensubstitutions‑Einstellungen für die Linux‑Plattform.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::LoadLinuxSettings()
```


## Beispiele



Zeigt, wie man auf Schriftart‑Substitutionstabellen für Windows und Linux zugreift.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Erstellt eine neue Tabellensubstitutions‑Regel und lädt die Standard‑Microsoft‑Windows‑Schriftart‑Substitutionstabelle.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// Unter Windows ist der Standard‑Ersatz für die Schriftart "Times New Roman CE" die Schriftart "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Wir können die Tabelle im XML‑Dokumentformat speichern.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux hat seine eigene Substitutionstabelle.
// Es gibt mehrere Ersatz‑Schriftarten für "Times New Roman CE".
// Wenn der erste Ersatz, "FreeSerif", ebenfalls nicht verfügbar ist,
// wird diese Regel die anderen im Array durchlaufen, bis sie einen verfügbaren findet.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Speichere die Linux‑Substitutionstabelle im XML‑Dokumentformat mithilfe eines Streams.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## Siehe auch

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
