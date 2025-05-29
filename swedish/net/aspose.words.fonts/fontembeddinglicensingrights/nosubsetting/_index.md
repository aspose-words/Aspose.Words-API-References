---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: Aspose.Words för .NET
description: Upptäck licensrättigheterna för inbäddning av teckensnitt utan underinställningar. Säkerställ efterlevnad och skydda dina teckensnitt samtidigt som du förbättrar dina designprojekt.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

Indikerar begränsningen "Ingen delmängd".

```csharp
public bool NoSubsetting { get; }
```

## Anmärkningar

När den här flaggan är inställd får teckensnittet inte delmängderas före inbäddning. Andra inbäddningsrestriktioner gäller också.

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

* class [FontEmbeddingLicensingRights](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
