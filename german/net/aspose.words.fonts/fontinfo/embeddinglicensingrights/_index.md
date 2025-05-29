---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontInfo EmbeddingLicensingRights-Eigenschaft, um einfach auf Ihre eingebetteten Schriftart-Lizenzrechte zuzugreifen und diese zu verwalten und so eine nahtlose Designintegration zu ermöglichen.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

Ruft die Lizenzrechte für eingebettete Schriftarten ab.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Bemerkungen

Der Wert kann null sein, wenn die Schriftart nicht eingebettet ist.

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
