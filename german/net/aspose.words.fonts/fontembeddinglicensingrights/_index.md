---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.FontEmbeddingLicensingRights, um die Einbettungsrechte für Schriftarten mühelos zu verwalten und die Präsentation Ihres Dokuments zu verbessern.
type: docs
weight: 3310
url: /de/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

Stellt die Einbettungslizenzrechte für die Schriftart dar.

```csharp
public class FontEmbeddingLicensingRights
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | Gibt die Einschränkung „Nur Bitmap-Einbettung“ an. |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | Nutzungsberechtigungen. |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | Gibt die Einschränkung „Keine Untergruppenbildung“ an. |

## Bemerkungen

Um mehr zu erfahren, besuchen Sie die [Abschnitt zur OpenType-Spezifikation](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) auf dem Microsoft Typography-Portal.

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

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
