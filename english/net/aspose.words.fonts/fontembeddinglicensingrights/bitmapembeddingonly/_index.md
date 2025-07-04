---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words for .NET
description: Discover the FontEmbeddingLicensingRights BitmapEmbeddingOnly property, which ensures exclusive Bitmap embedding restrictions for enhanced design control.
type: docs
weight: 10
url: /net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

Indicates the "Bitmap embedding only" restriction.

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## Remarks

When this bit is set, only bitmaps contained in the font may be embedded. No outline data may be embedded. If there are no bitmaps available in the font, then the font is considered unembeddable and the embedding services will fail. Other embedding restrictions also apply.

## Examples

Shows how to get license rights information for embedded fonts (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// Get the list of document fonts.
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

### See Also

* class [FontEmbeddingLicensingRights](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
