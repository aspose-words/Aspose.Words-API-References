---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fonts.FontFallbackSettings för anpassningsbara alternativ för teckensnitt, vilket säkerställer sömlös dokumentrendering och förbättrad textvisning.
type: docs
weight: 3330
url: /sv/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Anger inställningar för alternativa teckensnitt.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FontFallbackSettings
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Skapar automatiskt reservinställningarna genom att skanna tillgängliga teckensnitt. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | Läser in reservinställningar från XML-strömmen. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | Laddar alternativa teckensnittsinställningar från XML-filen. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Laddar fördefinierade reservinställningar som imiterar Microsoft Words reservinställningar och använder Microsoft Office-teckensnitt. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Laddar fördefinierade reservinställningar som använder Google Noto-teckensnitt. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | Sparar de aktuella reservinställningarna för strömning. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | Sparar de aktuella reservinställningarna till filen. |

## Anmärkningar

Som standard initieras reservinställningar med fördefinierade inställningar som imiterar Microsoft Words reservinställningar.

## Exempel

Visar hur man distribuerar reservteckensnitt över Unicode-teckenkodintervall.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Konfigurera våra typsnittsinställningar så att de endast hämtar typsnitt från mappen "MyFonts".
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Anrop av metoden "BuildAutomatic" genererar ett reservschema som
// distribuerar tillgängliga teckensnitt över så många Unicode-teckenkoder som möjligt.
// I vårt fall har den bara åtkomst till de få teckensnitt som finns i mappen "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Vi kan också ladda ett anpassat substitutionsschema från en fil som denna.
// Detta schema tillämpar teckensnittet "AllegroOpen" över Unicode-blocken "0000-00ff", teckensnittet "AllegroOpen" över "0100-024f",
// och teckensnittet "M+ 2m" i alla andra intervall som andra teckensnitt i schemat inte täcker.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Skapa en dokumentbyggare och ställ in dess teckensnitt till ett som inte finns i någon av våra källor.
// Våra teckensnittsinställningar kommer att anropa reservschemat för tecken som vi skriver med det otillgängliga teckensnittet.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Använd byggaren för att skriva ut alla Unicode-tecken från 0x0021 till 0x052F,
// med beskrivande linjer som delar Unicode-block som vi definierade i vårt anpassade teckensnittsalternativ.
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
