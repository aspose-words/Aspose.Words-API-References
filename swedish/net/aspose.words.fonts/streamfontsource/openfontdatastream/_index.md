---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: Aspose.Words för .NET
description: StreamFontSource OpenFontDataStream metod. Den här metoden bör öppna flödet med teckensnittsdata på begäran i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Den här metoden bör öppna flödet med teckensnittsdata på begäran.

```csharp
public abstract Stream OpenFontDataStream()
```

### Returvärde

Typsnittsdataström.

## Anmärkningar

Strömmen kommer att stängas efter läsning. Det finns ingen anledning att stänga den explicit.

## Exempel

Visar hur man laddar typsnitt från stream.

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

* class [StreamFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
