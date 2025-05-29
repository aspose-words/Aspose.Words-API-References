---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: Aspose.Words für .NET
description: Entdecken Sie die Lizenzrechte für die Font-Einbettung ohne Subsetting. Stellen Sie die Konformität sicher und schützen Sie Ihre Schriftarten, während Sie Ihre Designprojekte optimieren.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

Gibt die Einschränkung „Keine Untergruppenbildung“ an.

```csharp
public bool NoSubsetting { get; }
```

## Bemerkungen

Wenn dieses Flag gesetzt ist, darf die Schriftart vor dem Einbetten nicht in Untergruppen unterteilt werden. Es gelten auch andere Einbettungsbeschränkungen .

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
