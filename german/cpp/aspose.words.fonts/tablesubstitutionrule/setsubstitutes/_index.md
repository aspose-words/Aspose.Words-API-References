---
title: "Methode Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes"
linktitle: "SetSubstitutes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Methode Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes. Überschreibt Ersatzschriftartnamen für einen angegebenen Originalschriftartnamen in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule::SetSubstitutes method


Überschreibt Ersatz‑Schriftartnamen für einen angegebenen Original‑Schriftartnamen.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| originalFontName | const System::String\& | Originaler Schriftartname. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | Liste alternativer Schriftartnamen. |

## Beispiele



Zeigt, wie Schriftart-Ersetzungsregeln festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Die standardmäßigen Schriftquellen enthalten die erste Schriftart, die das Dokument verwendet.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Die zweite Schriftart, "Amethysta", ist nicht verfügbar.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Wir können eine Schriftart-Ersetzungstabelle konfigurieren, die bestimmt
// welche Schriftarten Aspose.Words als Ersatz für nicht verfügbare Schriftarten verwendet.
// Legen Sie zwei Ersatzschriftarten für "Amethysta" fest: "Arvo" und "Courier New".
// Wenn der erste Ersatz nicht verfügbar ist, versucht Aspose.Words den zweiten Ersatz zu verwenden, und so weiter.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" ist nicht verfügbar, und die Ersetzungsregel besagt, dass die erste zu verwendende Ersatzschriftart "Arvo" ist.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" ist ebenfalls nicht verfügbar, aber "Courier New" ist es.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Das Ausgabedokument zeigt den Text, der die Schriftart "Amethysta" verwendet, formatiert mit "Courier New".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
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
