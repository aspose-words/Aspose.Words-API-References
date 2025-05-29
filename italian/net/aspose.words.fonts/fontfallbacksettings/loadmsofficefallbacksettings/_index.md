---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words per .NET
description: Scopri il metodo FontFallbackSettings LoadMsOfficeFallbackSettings per implementare facilmente impostazioni di fallback simili a quelle di Microsoft Word con i font di Office per un'integrazione perfetta.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Carica le impostazioni di fallback predefinite che imitano il fallback di Microsoft Word e utilizzano i font di Microsoft Office.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## Esempi

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
