---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution Methode"
linktitle: "get_TableSubstitution"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution Methode. Einstellungen, die mit der Tabellensubstitutionsregel in C++ zusammenhängen."
type: docs
weight: 6000
url: /de/cpp/aspose.words.fonts/fontsubstitutionsettings/get_tablesubstitution/
---
## FontSubstitutionSettings::get_TableSubstitution method


[Settings](../../../aspose.words.settings/) related to table substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_TableSubstitution() const
```


## Beispiele



Zeigt, wie man mit benutzerdefinierten Schriftart-Ersetzungstabellen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Erstellen Sie eine neue Tabellenersetzungsregel und laden Sie die standardmäßige Windows-Schriftart-Ersetzungstabelle.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// Wenn wir Schriftarten ausschließlich aus unserem Ordner auswählen, benötigen wir eine benutzerdefinierte Ersetzungstabelle.
// Wir werden keinen Zugriff mehr auf die Microsoft Windows-Schriftarten haben,
// wie "Arial" oder "Times New Roman", da sie in unserem neuen Schriftartenordner nicht existieren.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Unten sind zwei Möglichkeiten, eine Ersetzungstabelle aus einer Datei im lokalen Dateisystem zu laden.
// 1 -  Aus einem Stream:
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Direkt aus einer Datei:
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// Da wir keinen Zugriff mehr auf "Arial" haben, wird unsere Schriftarttabelle zunächst versuchen, sie durch "Nonexistent Font" zu ersetzen.
// Wir haben diese Schriftart nicht, sodass die Tabelle zur nächsten Ersetzung "Kreon" im Ordner "MyFonts" übergeht.
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// Wir können diese Tabelle programmgesteuert erweitern. Wir werden einen Eintrag hinzufügen, der "Times New Roman" durch "Arvo" ersetzt.
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Wir können mit AddSubstitutes() eine sekundäre Fallback‑Ersetzung für einen vorhandenen Schriftarteintrag hinzufügen.
// Falls "Arvo" nicht verfügbar ist, wird unsere Tabelle nach "M+ 2m" als zweiter Ersetzungsoption suchen.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() kann eine neue Liste von Ersetzungs‑Schriftarten für eine Schriftart festlegen.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Das Schreiben von Text in Schriftarten, auf die wir keinen Zugriff haben, löst unsere Ersetzungsregeln aus.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## Siehe auch

* Class [TableSubstitutionRule](../../tablesubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
