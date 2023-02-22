---
title: Class FontFallbackSettings
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fonts.FontFallbackSettings klass. Anger inställningar för reservmekanism för teckensnitt.
type: docs
weight: 2720
url: /sv/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Anger inställningar för reservmekanism för teckensnitt.

```csharp
public class FontFallbackSettings
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Skapar automatiskt reservinställningarna genom att skanna tillgängliga teckensnitt. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(Stream) | Laddar reservinställningar från XML-ström. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(string) | Läser in alternativa teckensnittsinställningar från XML-fil. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Laddar fördefinierade reservinställningar som efterliknar Microsoft Word reserv och använder Microsoft office-teckensnitt. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Laddar fördefinierade reservinställningar som använder Google Noto-teckensnitt. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(Stream) | Sparar de aktuella reservinställningarna för att streama. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(string) | Sparar de aktuella reservinställningarna i filen. |

### Anmärkningar

Som standard initieras reservinställningar med fördefinierade inställningar som efterliknar Microsoft Word reserv.

### Exempel

Visar hur man distribuerar reservteckensnitt över Unicode-teckenkodintervall.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Konfigurera våra teckensnittsinställningar till att endast källtypsnitt från mappen "MyFonts".
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Att anropa "BuildAutomatic"-metoden kommer att generera ett reservschema som
// distribuerar tillgängliga typsnitt över så många Unicode-teckenkoder som möjligt.
// I vårt fall har den bara tillgång till en handfull typsnitt i mappen "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Vi kan också ladda ett anpassat ersättningsschema från en fil som denna.
// Detta schema tillämpar typsnittet "AllegroOpen" över "0000-00ff" Unicode-blocken, "AllegroOpen"-teckensnittet över "0100-024f",
// och typsnittet "M+ 2m" i alla andra intervall som andra typsnitt i schemat inte täcker.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Skapa en dokumentbyggare och ställ in dess teckensnitt till ett som inte finns i någon av våra källor.
// Våra teckensnittsinställningar kommer att anropa reservschemat för tecken som vi skriver med det otillgängliga teckensnittet.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Använd byggaren för att skriva ut varje Unicode-tecken från 0x0021 till 0x052F,
// med beskrivande linjer som delar Unicode-block som vi definierade i vårt anpassade typsnittsalternativ.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### Se även

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)


