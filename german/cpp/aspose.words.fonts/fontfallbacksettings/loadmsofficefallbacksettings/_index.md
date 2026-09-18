---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings Methode"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings Methode. Lädt vordefinierte Fallback‑Einstellungen, die das Microsoft‑Word‑Fallback nachahmen und Microsoft‑Office‑Schriften in C++ verwenden."
type: docs
weight: 6000
url: /de/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


Lädt vordefinierte Fallback‑Einstellungen, die das Microsoft‑Word‑Fallback nachahmen und Microsoft‑Office‑Schriftarten verwenden.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## Beispiele



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
