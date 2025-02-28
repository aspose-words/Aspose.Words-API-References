---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words for .NET
description: Discover the FontInfo EmbeddingLicensingRights property to easily access and manage your embedded font licensing rights for seamless design integration.
type: docs
weight: 30
url: /net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

Gets the embedded font licensing rights.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Remarks

The value may be null if font is not embedded.

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
