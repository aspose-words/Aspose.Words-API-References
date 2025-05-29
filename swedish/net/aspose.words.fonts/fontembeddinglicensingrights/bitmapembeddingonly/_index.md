---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FontEmbeddingLicensingRights BitmapEmbeddingOnly, som säkerställer exklusiva begränsningar för bitmappsinbäddning för förbättrad designkontroll.
type: docs
weight: 10
url: /sv/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

Indikerar begränsningen "Endast bitmappsinbäddning".

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## Anmärkningar

När den här biten är inställd kan endast bitmappar som finns i teckensnittet bäddas in. Inga konturdata får bäddas in. Om det inte finns några bitmappar tillgängliga i teckensnittet anses teckensnittet vara omöjligt att bädda in och embedding -tjänsterna kommer att misslyckas. Andra inbäddningsbegränsningar gäller också.

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
