---
title: "Metodo Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings"
linktitle: "LoadNotoFallbackSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings. Carica le impostazioni di fallback predefinite che utilizzano i font Google Noto in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


Carica le impostazioni di fallback predefinite che utilizzano i font Google Noto.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## Esempi



Mostra come aggiungere impostazioni di fallback dei caratteri predefinite per i font Google Noto.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// Questi sono font gratuiti concessi in licenza sotto la SIL Open Font License.
// Possiamo scaricare i font qui:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// Nota che le impostazioni predefinite utilizzano solo font Noto di tipo Sans con peso normale.
// Alcuni dei font Noto utilizzano funzionalità tipografiche avanzate.
// I font con tipografia avanzata potrebbero non essere renderizzati correttamente poiché Aspose.Words attualmente non li supporta.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


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
