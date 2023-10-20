---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: Aspose.Words per .NET
description: FontFallbackSettings LoadNotoFallbackSettings metodo. Carica le impostazioni di fallback predefinite che utilizzano i caratteri Google Noto in C#.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Carica le impostazioni di fallback predefinite che utilizzano i caratteri Google Noto.

```csharp
public void LoadNotoFallbackSettings()
```

## Esempi

Mostra come aggiungere impostazioni di fallback dei caratteri predefinite per i caratteri di Google Noto.

```csharp
FontSettings fontSettings = new FontSettings();

// Questi sono font gratuiti concessi in licenza con la licenza SIL Open Font.
// Possiamo scaricare i caratteri qui:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // Tieni presente che le impostazioni predefinite utilizzano solo caratteri Noto in stile Sans con peso regolare.
// Alcuni caratteri Noto utilizzano funzionalità tipografiche avanzate.
// I caratteri con tipografia avanzata potrebbero non essere visualizzati correttamente poiché Aspose.Words attualmente non li supporta.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

Mostra come caricare le impostazioni predefinite dei caratteri di fallback.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Salva lo schema dei caratteri di fallback predefinito in un documento XML.
// Ad esempio, uno degli elementi ha un valore "0C00-0C7F" per Range e un valore "Vani" corrispondente per FallbackFonts.
// Ciò significa che se il carattere utilizzato da parte del testo non contiene simboli per il blocco Unicode 0x0C00-0x0C7F,
// lo schema di fallback utilizzerà i simboli del sostituto del carattere "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Di seguito sono riportati due schemi di fallback dei caratteri predefiniti tra cui possiamo scegliere.
// 1 - Utilizza lo schema predefinito di Microsoft Office, che è lo stesso di quello predefinito:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Utilizza lo schema creato dai caratteri Google Noto:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Guarda anche

* class [FontFallbackSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
