---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings-Methode"
linktitle: "LoadNotoFallbackSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings-Methode. Lädt vordefinierte Fallback-Einstellungen, die Google Noto-Schriften in C++ verwenden."
type: docs
weight: 7000
url: /de/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


Lädt vordefinierte Fallback‑Einstellungen, die Google‑Noto‑Schriftarten verwenden.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## Beispiele



Zeigt, wie man vordefinierte Schrift-Fallback-Einstellungen für Google Noto-Schriften hinzufügt.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// Dies sind kostenlose Schriften, die unter der SIL Open Font License lizenziert sind.
// Wir können die Schriften hier herunterladen:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// Beachten Sie, dass die vordefinierten Einstellungen nur Sans-Stil Noto-Schriften mit normaler Stärke verwenden.
// Einige der Noto-Schriften verwenden erweiterte typografische Funktionen.
// Schriften mit fortgeschrittener Typografie werden möglicherweise nicht korrekt dargestellt, da Aspose.Words sie derzeit nicht unterstützt.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


Zeigt, wie vordefinierte Fallback-Schrifteinstellungen geladen werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Speichert das standardmäßige Fallback-Schriftartenschema in ein XML-Dokument.
// Zum Beispiel hat eines der Elemente den Wert "0C00-0C7F" für Range und den entsprechenden Wert "Vani" für FallbackFonts.
// Das bedeutet, dass wenn die Schrift, die ein Text verwendet, keine Symbole für den Unicode‑Block 0x0C00-0x0C7F enthält,
// das Fallback‑Schema Symbole aus der Schriftart‑Ersatz "Vani" verwendet.
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// Unten sind zwei vordefinierte Schrift‑Fallback‑Schemata aufgeführt, aus denen wir wählen können.
// 1 -  Verwenden Sie das standardmäßige Microsoft‑Office‑Schema, das dem Standard entspricht:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  Verwenden Sie das aus Google‑Noto‑Schriften erstellte Schema:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## Siehe auch

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
