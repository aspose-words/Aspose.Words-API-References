---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.FontEmbeddingLicensingRights för att enkelt hantera rättigheter för inbäddning av teckensnitt och förbättra presentationen av ditt dokument.
type: docs
weight: 3310
url: /sv/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

Representerar inbäddningslicensrättigheter för teckensnittet.

```csharp
public class FontEmbeddingLicensingRights
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | Indikerar begränsningen "Endast bitmappsinbäddning". |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | Användarbehörigheter. |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | Indikerar begränsningen "Ingen delmängd". |

## Anmärkningar

För att läsa mer, besök [OpenType-specifikationsavsnitt](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) på Microsoft Typography-portalen.

## Exempel

Visar hur man får information om licensrättigheter för inbäddade teckensnitt (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// Hämta listan över dokumentfonter.
FontInfoCollection fontInfos = doc.FontInfos;
foreach (FontInfo fontInfo in fontInfos) 
{
    if (fontInfo.EmbeddingLicensingRights != null)
    {
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.EmbeddingUsagePermissions);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.BitmapEmbeddingOnly);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.NoSubsetting);
    }
}
```

### Se även

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
