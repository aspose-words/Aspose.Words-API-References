---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
second_title: Aspose.Words per .NET API Reference
description: FontFallbackSettings metodo. Carica impostazioni di fallback predefinite che imitano il fallback di Microsoft Word e utilizzano i caratteri di Microsoft Office.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Carica impostazioni di fallback predefinite che imitano il fallback di Microsoft Word e utilizzano i caratteri di Microsoft Office.

```csharp
public void LoadMsOfficeFallbackSettings()
```

### Esempi

Mostra come caricare le impostazioni dei caratteri di fallback predefinite.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Salva lo schema dei caratteri di fallback predefinito in un documento XML.
// Ad esempio, uno degli elementi ha un valore di "0C00-0C7F" per Range e un valore "Vani" corrispondente per FallbackFonts.
// Ciò significa che se il carattere utilizzato da alcuni testi non ha simboli per il blocco Unicode 0x0C00-0x0C7F,
// lo schema di fallback utilizzerà i simboli del sostituto del carattere "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Di seguito sono riportati due schemi di font di riserva predefiniti tra cui possiamo scegliere.
// 1 - Utilizza lo schema predefinito di Microsoft Office, che è lo stesso di quello predefinito:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Usa lo schema creato dai caratteri di Google Noto:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Guarda anche

* class [FontFallbackSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontfallbacksettings/)
* assemblea [Aspose.Words](../../../)


