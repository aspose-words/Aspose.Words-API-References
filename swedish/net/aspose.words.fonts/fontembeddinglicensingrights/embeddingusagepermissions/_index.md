---
title: FontEmbeddingLicensingRights.EmbeddingUsagePermissions
linktitle: EmbeddingUsagePermissions
articleTitle: EmbeddingUsagePermissions
second_title: Aspose.Words för .NET
description: Frigör kreativ potential med licensrättigheter för inbäddning av teckensnitt. Utforska användningsbehörigheter för sömlös teckensnittsintegration i dina projekt.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/
---
## FontEmbeddingLicensingRights.EmbeddingUsagePermissions property

Användarbehörigheter.

```csharp
public FontEmbeddingUsagePermissions EmbeddingUsagePermissions { get; }
```

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

* enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* class [FontEmbeddingLicensingRights](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
