---
title: FontFallbackSettings.LoadNotoFallbackSettings
second_title: Aspose.Words för .NET API Referens
description: FontFallbackSettings metod. Laddar fördefinierade reservinställningar som använder Google Nototeckensnitt.
type: docs
weight: 40
url: /sv/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Laddar fördefinierade reservinställningar som använder Google Noto-teckensnitt.

```csharp
public void LoadNotoFallbackSettings()
```

### Exempel

Visar hur man lägger till fördefinierade alternativa teckensnittsinställningar för Google Noto-teckensnitt.

```csharp
FontSettings fontSettings = new FontSettings();

// Dessa är gratis typsnitt licensierade under SIL Open Font License.
// Vi kan ladda ner typsnitten här:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

  // Observera att de fördefinierade inställningarna endast använder Sans-stil Noto-teckensnitt med normal vikt.
// Vissa av Noto-teckensnitten använder avancerade typografifunktioner.
// Teckensnitt med avancerad typografi kanske inte renderas korrekt eftersom Aspose.Words för närvarande inte stöder dem.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

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
* namnutrymme [Aspose.Words.Fonts](../../fontfallbacksettings/)
* hopsättning [Aspose.Words](../../../)


