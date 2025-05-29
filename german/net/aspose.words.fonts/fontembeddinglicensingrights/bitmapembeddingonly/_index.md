---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft FontEmbeddingLicensingRights BitmapEmbeddingOnly, die exklusive Bitmap-Einbettungsbeschränkungen für eine verbesserte Designkontrolle gewährleistet.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

Gibt die Einschränkung „Nur Bitmap-Einbettung“ an.

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## Bemerkungen

Wenn dieses Bit gesetzt ist, können nur in der Schriftart enthaltene Bitmaps eingebettet werden. Es dürfen keine Konturdaten eingebettet werden. Wenn in der Schriftart keine Bitmaps verfügbar sind, gilt die Schriftart als nicht einbettbar und die Einbettungsdienste schlagen fehl. Es gelten auch andere Einbettungsbeschränkungen.

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

* class [FontEmbeddingLicensingRights](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
