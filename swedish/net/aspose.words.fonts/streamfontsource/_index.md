---
title: Class StreamFontSource
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fonts.StreamFontSource klass. Basklass för användardefinierad strömteckensnittskälla.
type: docs
weight: 2860
url: /sv/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Basklass för användardefinierad strömteckensnittskälla.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Nyckeln till denna källa i cachen. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittskällans prioritet. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Returnerar typen av teckensnittskälla. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskällan när ett problem upptäcks som kan resultera i förlust av formatering. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via den här källan. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Den här metoden bör öppna flödet med teckensnittsdata på begäran. |

### Anmärkningar

För att använda strömfontkällan bör du skapa en härledd klass från`StreamFontSource` och tillhandahålla implementering av[`OpenFontDataStream`](./openfontdatastream/) metod.

[`OpenFontDataStream`](./openfontdatastream/)metod kan kallas flera gånger. För första gången kommer det att kallas när Aspose.Words skannar de medföljande teckensnittskällorna för att få en lista över tillgängliga teckensnitt. Senare kan det kallas om teckensnittet används i dokumentet för att analysera teckensnittsdata och för att bädda in teckensnittsdata i vissa utdataformat.

`StreamFontSource` kan vara användbart eftersom det gör det möjligt att ladda teckensnittsdata endast när det krävs och inte lagra det i minnet för[`FontSettings`](../fontsettings/) livstid.

### Exempel

Visar hur man laddar typsnitt från stream.

```csharp
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// Ladda teckensnittsdata endast när det behövs istället för att lagra det i minnet
/// under hela livslängden för objektet "FontSettings".
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### Se även

* class [FontSourceBase](../fontsourcebase/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)


