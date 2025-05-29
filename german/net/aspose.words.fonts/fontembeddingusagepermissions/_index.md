---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Fonts.FontEmbeddingUsagePermissions, die eine präzise Kontrolle über die Berechtigungen zum Einbetten von Schriftarten für eine verbesserte Dokumentenverwaltung ermöglicht.
type: docs
weight: 3320
url: /de/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

Stellt die Nutzungsberechtigungen für die Schriftarteinbettung dar.

```csharp
public enum FontEmbeddingUsagePermissions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Installable | `0` | Die Schriftart kann eingebettet und dauerhaft installiert werden, um sie auf Remote-Systemen oder durch andere Benutzer zu verwenden. |
| RestrictedLicense | `1` | Die Schriftart darf ohne vorherige ausdrückliche Genehmigung des rechtmäßigen Eigentümers in keiner Weise geändert, eingebettet oder ausgetauscht werden. |
| PrintAndPreview | `2` | Die Schriftart kann eingebettet und vorübergehend auf anderen Systemen geladen werden, um das Dokument anzuzeigen oder auszudrucken. |
| Editable | `3` | Die Schriftart kann eingebettet und vorübergehend auf anderen Systemen geladen werden. |

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
