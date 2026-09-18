---
title: "Aspose::Words::Fonts::SystemFontSource Klasse"
linktitle: "SystemFontSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::SystemFontSource Klasse. Stellt alle im System installierten TrueType-Schriftarten dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class


Stellt alle im System installierten TrueType-Schriftarten dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class SystemFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Priority](../fontsourcebase/get_priority/)() const | Gibt die Priorität der Schriftquellen zurück. |
| [get_Type](./get_type/)() override | Gibt den Typ der Schriftquelle zurück. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriften zurück. |
| static [GetSystemFontFolders](./getsystemfontfolders/)() | Gibt System-Schriftordner zurück oder ein leeres Array, wenn die Ordner nicht zugänglich sind. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| [SystemFontSource](./systemfontsource/)() | Konstruktor. |
| [SystemFontSource](./systemfontsource/)(int32_t) | Konstruktor. |
| static [Type](./type/)() |  |

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

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
