---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Fonts.FontEmbeddingUsagePermissions, som möjliggör exakt kontroll över behörigheter för inbäddning av teckensnitt för förbättrad dokumenthantering.
type: docs
weight: 3320
url: /sv/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

Representerar behörigheterna för användning av teckensnittsinbäddning.

```csharp
public enum FontEmbeddingUsagePermissions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Installable | `0` | Typsnittet kan vara inbäddat och permanent installerat för användning på fjärrsystem eller för användning av andra användare. |
| RestrictedLicense | `1` | Typsnittet får inte modifieras, bäddas in eller bytas ut på något sätt utan att först inhämta uttryckligt tillstånd från den juridiska ägaren. |
| PrintAndPreview | `2` | Typsnittet kan vara inbäddat och kan tillfälligt laddas på andra system för att visa eller skriva ut dokumentet. |
| Editable | `3` | Typsnittet kan vara inbäddat och kan laddas tillfälligt på andra system. |

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
