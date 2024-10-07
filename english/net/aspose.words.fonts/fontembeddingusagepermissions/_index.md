---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.FontEmbeddingUsagePermissions enum. Represents the font embedding usage permissions in C#.
type: docs
weight: 3180
url: /net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

Represents the font embedding usage permissions.

```csharp
public enum FontEmbeddingUsagePermissions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Installable | `0` | The font may be embedded, and may be permanently installed for use on a remote systems, or for use by other users. |
| RestrictedLicense | `1` | The font must not be modified, embedded or exchanged in any manner without first obtaining explicit permission of the legal owner. |
| PrintAndPreview | `2` | The font may be embedded, and may be temporarily loaded on other systems for purposes of viewing or printing the document. |
| Editable | `3` | The font may be embedded, and may be temporarily loaded on other systems. |

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

* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
