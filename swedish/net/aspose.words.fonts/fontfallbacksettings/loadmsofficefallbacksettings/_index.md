---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words för .NET
description: Upptäck metoden FontFallbackSettings LoadMsOfficeFallbackSettings för att enkelt implementera Microsoft Word-liknande reservinställningar med Office-teckensnitt för sömlös integration.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Laddar fördefinierade reservinställningar som imiterar Microsoft Words reservinställningar och använder Microsoft Office-teckensnitt.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## Exempel

Visar hur man laddar fördefinierade inställningar för reservteckensnitt.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Spara standardteckensnittsschemat till ett XML-dokument.
// Till exempel har ett av elementen värdet "0C00-0C7F" för Range och ett motsvarande "Vani"-värde för FallbackFonts.
// Detta betyder att om teckensnittet som viss text använder inte har symboler för Unicode-blocket 0x0C00-0x0C7F,
// reservschemat kommer att använda symboler från typsnittsersättningen "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Nedan finns två fördefinierade teckensnittsalternativ som vi kan välja mellan.
// 1 - Använd standardschemat för Microsoft Office, vilket är samma som standardschemat:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Använd schemat som byggts från Google Noto-teckensnitt:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Se även

* class [FontFallbackSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
