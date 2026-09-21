---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings metod"
linktitle: "LoadNotoFallbackSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings metod. Laddar fördefinierade fallback‑inställningar som använder Google Noto‑teckensnitt i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


Läser in fördefinierade fallback‑inställningar som använder Google Noto‑typsnitt.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## Exempel



Visar hur man lägger till fördefinierade teckensnittsfallback‑inställningar för Google Noto‑teckensnitt.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// Detta är gratis teckensnitt licensierade under SIL Open Font License.
// Vi kan ladda ner teckensnitten här:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// Observera att de fördefinierade inställningarna endast använder Sans‑stil Noto‑teckensnitt med normal vikt.
// Vissa av Noto‑teckensnitten använder avancerade typografifunktioner.
// Teckensnitt med avancerad typografi kanske inte renderas korrekt eftersom Aspose.Words för närvarande inte stöder dem.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


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
