---
title: PhysicalFontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words für .NET
description: Entdecken Sie die PhysicalFontInfo EmbeddingLicensingRights-Eigenschaft – schalten Sie wichtige Schriftarteneinbettungsrechte für eine nahtlose Designintegration frei.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/
---
## PhysicalFontInfo.EmbeddingLicensingRights property

Einbettungslizenzrechte für die Schriftart.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Beispiele

Zeigt, wie Sie Lizenzrechteinformationen für eingebettete Schriftarten erhalten (PhysicalFontInfo).

```csharp
FontSettings settings = FontSettings.DefaultInstance;
FontSourceBase source = settings.GetFontsSources()[0];

// Liste der verfügbaren Schriftarten abrufen.
IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();
foreach (PhysicalFontInfo fontInfo in fontInfos)
{
    if (fontInfo.EmbeddingLicensingRights != null)
    {
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.EmbeddingUsagePermissions);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.BitmapEmbeddingOnly);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.NoSubsetting);
    }
}
```

### Siehe auch

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [PhysicalFontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
