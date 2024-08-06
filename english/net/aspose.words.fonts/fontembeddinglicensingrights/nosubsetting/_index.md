---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: Aspose.Words for .NET
description: FontEmbeddingLicensingRights NoSubsetting property. Indicates the No subsetting restriction in C#.
type: docs
weight: 30
url: /net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

Indicates the "No subsetting" restriction.

```csharp
public bool NoSubsetting { get; }
```

## Remarks

When this flag is set, the font must not be subsetted prior to embedding. Other embedding restrictions also apply.

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
