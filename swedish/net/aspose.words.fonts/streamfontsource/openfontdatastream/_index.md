---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: Aspose.Words för .NET
description: Upptäck StreamFontSource OpenFontDataStream-metoden för att effektivt komma åt teckensnittsdataströmmar på begäran, vilket förbättrar ditt designarbetsflöde.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Den här metoden bör öppna strömmen med teckensnittsdata på begäran.

```csharp
public abstract Stream OpenFontDataStream()
```

### Returvärde

Dataström för teckensnitt.

## Anmärkningar

Strömmen kommer att stängas efter läsning. Det finns inget behov av att stänga den explicit.

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

* class [StreamFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
