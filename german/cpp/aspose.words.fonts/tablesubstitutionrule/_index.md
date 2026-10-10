---
title: "Aspose::Words::Fonts::TableSubstitutionRule Klasse"
linktitle: "TableSubstitutionRule"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::TableSubstitutionRule Klasse. Regel für die Schriftart-Substitution in Tabellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 18000
url: /de/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


Tabellen-Schriftart-Ersetzungsregel. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Fügt Ersatzschriftartnamen für einen angegebenen Originalschriftartnamen hinzu. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Gibt an, ob die Regel aktiviert ist oder nicht. |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | Gibt ein Array zurück, das Ersatzschriftartnamen für den angegebenen Originalschriftartnamen enthält. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | Lädt Tabellensubstitutions‑Einstellungen aus einer XML‑Datei. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | Lädt Tabellensubstitutions‑Einstellungen aus einem XML‑Stream. |
| [LoadAndroidSettings](./loadandroidsettings/)() | Lädt vordefinierte Tabellensubstitutions‑Einstellungen für die Android‑Plattform. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | Lädt vordefinierte Tabellensubstitutions‑Einstellungen für die Linux‑Plattform. |
| [LoadWindowsSettings](./loadwindowssettings/)() | Lädt vordefinierte Tabellensubstitutions‑Einstellungen für die Windows‑Plattform. |
| [Save](./save/)(const System::String\&) | Speichert die aktuellen Tabellensubstitutions‑Einstellungen in einer Datei. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Speichert die aktuellen Tabellensubstitutions‑Einstellungen in einen Stream. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Setter für [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Überschreibt Ersatz‑Schriftartnamen für einen angegebenen Original‑Schriftartnamen. |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
