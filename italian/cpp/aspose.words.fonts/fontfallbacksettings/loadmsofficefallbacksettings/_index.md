---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings method"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings method. Carica le impostazioni di fallback predefinite che imitano il fallback di Microsoft Word e utilizza i caratteri Microsoft Office in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


Carica le impostazioni di fallback predefinite che imitano il fallback di Microsoft Word e utilizzano i font di Microsoft Office.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## Esempi



Mostra come caricare le impostazioni di fallback dei font predefinite.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Salva lo schema di fallback dei caratteri predefinito in un documento XML.
// Ad esempio, uno degli elementi ha un valore "0C00-0C7F" per Intervallo e un valore corrispondente "Vani" per FallbackFonts.
// Ciò significa che se il carattere utilizzato da qualche testo non ha simboli per il blocco Unicode 0x0C00-0x0C7F,
// lo schema di fallback utilizzerà i simboli dal sostituto del carattere "Vani".
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// Di seguito sono riportati due schemi di fallback dei caratteri predefiniti tra cui possiamo scegliere.
// 1 -  Usa lo schema predefinito di Microsoft Office, che è lo stesso di quello predefinito:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  Usa lo schema costruito con i caratteri Google Noto:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## Vedi anche

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
