---
title: "Aspose::Words::Fonts::FontSubstitutionSettings class"
linktitle: "FontSubstitutionSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSubstitutionSettings class. Gibt die Einstellungen des Schriftart‑Ersetzungsmechanismus an. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class


Gibt die Einstellungen des Schriftart-Ersetzungsmechanismus an. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionSettings : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DefaultFontSubstitution](./get_defaultfontsubstitution/)() const | [Settings](../../aspose.words.settings/) bezogen auf die Standard‑Schriftart‑Ersetzungsregel. |
| [get_FontConfigSubstitution](./get_fontconfigsubstitution/)() const | [Settings](../../aspose.words.settings/) bezogen auf die Schrift‑Konfigurations‑Ersetzungsregel. |
| [get_FontInfoSubstitution](./get_fontinfosubstitution/)() const | [Settings](../../aspose.words.settings/) bezogen auf die Schrift‑Info‑Ersetzungsregel. |
| [get_FontNameSubstitution](./get_fontnamesubstitution/)() const | [Settings](../../aspose.words.settings/) bezogen auf die Schrift‑Namens‑Ersetzungsregel. |
| [get_TableSubstitution](./get_tablesubstitution/)() const | [Settings](../../aspose.words.settings/) bezogen auf die Tabellen‑Ersetzungsregel. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Hinweise


[Font](../../aspose.words/font/) substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

Die Reihenfolge der Regeln ist wie folgt:1. [Font](../../aspose.words/font/) Namens‑Ersetzungsregel (standardmäßig aktiviert)
1. [Font](../../aspose.words/font/) Konfigurations‑Ersetzungsregel (standardmäßig deaktiviert)
1. Tabellen‑Ersetzungsregel (standardmäßig aktiviert)
1. [Font](../../aspose.words/font/) Info‑Ersetzungsregel (standardmäßig aktiviert)
1. Standard‑Schriftart‑Regel (standardmäßig aktiviert)



Hinweis: Die Schrift‑Info‑Ersetzungsregel löst die Schriftart immer auf, wenn [FontInfo](../fontinfo/) verfügbar ist, und überschreibt die Standard‑Schriftart‑Regel. Wenn Sie die Standard‑Schriftart‑Regel verwenden möchten, sollten Sie die Schrift‑Info‑Ersetzungsregel deaktivieren.

Hinweis: Die Schrift‑Konfigurations‑Ersetzungsregel löst die Schriftart in den meisten Fällen auf und überschreibt daher alle anderen Regeln.

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

## Siehe auch

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
