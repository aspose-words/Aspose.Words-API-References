---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.StreamFontSource, din lösning för anpassade strömmande teckensnittskällor som förbättrar dokumentflexibiliteten och designen.
type: docs
weight: 3470
url: /sv/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Basklass för användardefinierad strömfontkälla.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Nyckeln till denna källa i cachen. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittets källprioritet. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Returnerar typen av teckensnittskällan. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskälla när ett problem upptäcks som kan leda till förlust av formateringstillverkning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Den här metoden bör öppna strömmen med teckensnittsdata på begäran. |

## Anmärkningar

För att kunna använda strömfontkällan bör du skapa en härledd klass från`StreamFontSource` och tillhandahålla implementering av[`OpenFontDataStream`](./openfontdatastream/) metod.

[`OpenFontDataStream`](./openfontdatastream/)Metoden kan anropas flera gånger. För första gången kommer den att anropas när Aspose.Words skannar de angivna teckensnittskällorna för att hämta en lista över tillgängliga teckensnitt. Senare kan den anropas om teckensnittet används i dokumentet för att analysera teckensnittsdata och bädda in teckensnittsdata i vissa utdataformat.

`StreamFontSource` kan vara användbart eftersom det tillåter att teckensnittsdata endast laddas när det behövs och inte lagras i minnet för[`FontSettings`](../fontsettings/) livstid.

## Exempel

Visar hur man laddar teckensnitt från strömmen.

```csharp
public void StreamFontSourceFileRendering()
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
/// Ladda endast teckensnittsdata när det behövs istället för att lagra dem i minnet
/// för hela livslängden för "FontSettings"-objektet.
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
* interface [  ](../../global/%02  /)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
