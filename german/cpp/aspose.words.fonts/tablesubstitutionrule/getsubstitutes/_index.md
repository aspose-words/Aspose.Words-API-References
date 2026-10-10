---
title: "Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes method"
linktitle: "GetSubstitutes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes-Methode. Gibt ein Array zurück, das Ersatzschriftartnamen für den angegebenen Originalschriftartnamen in C++ enthält."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fonts/tablesubstitutionrule/getsubstitutes/
---
## TableSubstitutionRule::GetSubstitutes method


Gibt ein Array zurück, das Ersatzschriftartnamen für den angegebenen Originalschriftartnamen enthält.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerable<System::String>> Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes(const System::String &originalFontName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| originalFontName | const System::String\& | Originaler Schriftartname. |

### ReturnValue

Liste alternativer Schriftartnamen.

## Beispiele



Zeigt, wie man auf die System-Schriftquelle eines Dokuments zugreift und Schriftersatz festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Standardmäßig enthält ein leeres Dokument immer eine System-Schriftquelle.
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

// Legen Sie eine Schriftart, die im Windows-Schriftartenverzeichnis vorhanden ist, als Ersatz für eine nicht vorhandene fest.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// Alternativ könnten wir eine Ordner-Schriftquelle hinzufügen, in der der entsprechende Ordner die Schriftart enthält.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// Das Zurücksetzen der Schriftquellen lässt uns weiterhin die System-Schriftquelle sowie unsere Ersatzschriften.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
