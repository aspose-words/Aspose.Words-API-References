---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words för .NET
description: FontFallbackSettings LoadMsOfficeFallbackSettings metod. Laddar fördefinierade reservinställningar som efterliknar Microsoft Word reserv och använder Microsoft officeteckensnitt i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Laddar fördefinierade reservinställningar som efterliknar Microsoft Word reserv och använder Microsoft office-teckensnitt.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## Exempel

Visar hur man laddar fördefinierade reservteckensnittsinställningar.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Spara standardtypsnittsschemat i ett XML-dokument.
// Till exempel har ett av elementen värdet "0C00-0C7F" för Range och ett motsvarande "Vani"-värde för FallbackFonts.
// Detta betyder att om typsnittet som någon text använder inte har symboler för 0x0C00-0x0C7F Unicode-blocket,
// reservschemat kommer att använda symboler från "Vani" teckensnittsersättning.
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Nedan finns två fördefinierade typsnittsalternativ som vi kan välja mellan.
// 1 - Använd standardschemat för Microsoft Office, vilket är samma som standardschemat:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Använd schemat byggt från Google Noto-teckensnitt:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Se även

* class [FontFallbackSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
