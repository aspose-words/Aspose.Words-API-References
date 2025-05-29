---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: Aspose.Words per .NET
description: Scopri come migliorare la tua tipografia con il metodo LoadNotoFallbackSettings di FontFallbackSettings, utilizzando i font Google Noto per una visualizzazione fluida del testo.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Carica le impostazioni di fallback predefinite che utilizzano i font Google Noto.

```csharp
public void LoadNotoFallbackSettings()
```

## Esempi

Mostra come aggiungere impostazioni predefinite di fallback per i font Google Noto.

```csharp
FontSettings fontSettings = new FontSettings();

// Questi sono font gratuiti concessi in licenza secondo la SIL Open Font License.
// Possiamo scaricare i font qui:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // Nota che le impostazioni predefinite utilizzano solo font Noto in stile Sans con peso normale.
// Alcuni font Noto utilizzano funzionalità tipografiche avanzate.
// I font dotati di tipografia avanzata potrebbero non essere riprodotti correttamente poiché Aspose.Words al momento non li supporta.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

Mostra come caricare le impostazioni predefinite dei font di fallback.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Salva lo schema di font di fallback predefinito in un documento XML.
// Ad esempio, uno degli elementi ha un valore di "0C00-0C7F" per Range e un valore corrispondente di "Vani" per FallbackFonts.
// Ciò significa che se il font utilizzato in un testo non contiene simboli per il blocco Unicode 0x0C00-0x0C7F,
// lo schema di fallback utilizzerà i simboli del sostituto del font "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Di seguito sono riportati due schemi di fallback dei font predefiniti tra cui possiamo scegliere.
// 1 - Utilizza lo schema predefinito di Microsoft Office, che è lo stesso predefinito:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Utilizza lo schema creato dai font Google Noto:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Guarda anche

* class [FontFallbackSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
