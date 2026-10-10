---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings method"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings method. Laddar fördefinierade fallback‑inställningar som efterliknar Microsoft Word‑fallback och använder Microsoft Office‑teckensnitt i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


Läser in fördefinierade fallback‑inställningar som efterliknar Microsoft Word-fallback och använder Microsoft Office‑typsnitt.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## Exempel



Visar hur man laddar fördefinierade fallback‑teckensnittinställningar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Spara standardfallback‑teckensnittsschemat till ett XML‑dokument.
// Till exempel har ett av elementen värdet "0C00-0C7F" för Range och ett motsvarande "Vani"‑värde för FallbackFonts.
// Detta betyder att om teckensnittet som någon text använder inte har symboler för Unicode‑blocket 0x0C00-0x0C7F,
// fallback‑schemat kommer att använda symboler från "Vani"-teckensnittet som ersättning.
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// Nedan finns två fördefinierade teckensnittsfallback‑scheman som vi kan välja mellan.
// 1 -  Använd standard Microsoft Office‑schemat, som är detsamma som standarden:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  Använd schemat som är byggt från Google Noto‑teckensnitt:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## Se även

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
