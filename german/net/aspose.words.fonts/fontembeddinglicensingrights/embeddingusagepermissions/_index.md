---
title: FontEmbeddingLicensingRights.EmbeddingUsagePermissions
linktitle: EmbeddingUsagePermissions
articleTitle: EmbeddingUsagePermissions
second_title: Aspose.Words für .NET
description: Entfesseln Sie Ihr kreatives Potenzial mit Lizenzrechten für die Einbettung von Schriftarten. Informieren Sie sich über Nutzungsrechte für die nahtlose Integration von Schriftarten in Ihre Projekte.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/
---
## FontEmbeddingLicensingRights.EmbeddingUsagePermissions property

Nutzungsberechtigungen.

```csharp
public FontEmbeddingUsagePermissions EmbeddingUsagePermissions { get; }
```

## Beispiele

Zeigt, wie Sie Lizenzrechtsinformationen für eingebettete Schriftarten erhalten (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// Liste der Dokumentschriftarten abrufen.
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

### Siehe auch

* enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* class [FontEmbeddingLicensingRights](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
