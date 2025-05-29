---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Saving.Zip64Mode für die effiziente Verwendung des ZIP64-Formats in OOXML-Dateien, wodurch die Dateigrößenverwaltung und Kompatibilität verbessert wird.
type: docs
weight: 6550
url: /de/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

Gibt an, wann ZIP64-Formaterweiterungen für OOXML-Dateien verwendet werden sollen.

```csharp
public enum Zip64Mode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Never | `0` | Verwenden Sie keine ZIP64-Formaterweiterungen. |
| IfNecessary | `1` | Verwenden Sie bei Bedarf ZIP64-Formaterweiterungen. |
| Always | `2` | Verwenden Sie immer ZIP64-Formaterweiterungen. |

## Bemerkungen

Eine OOXML-Datei ist ein ZIP-Archiv mit einer Beschränkung der unkomprimierten Dateigröße auf 4 GB (2^32 Bytes), die komprimierte Dateigröße und die Gesamtgröße des Archivs sowie einer Beschränkung von 65.535 (2^16-1) Dateien im Archiv. ZIP64-Formaterweiterungen erhöhen die Beschränkung auf 2^64.

## Beispiele

Zeigt, wie ZIP64-Formaterweiterungen verwendet werden.

```csharp
Random random = new Random();
DocumentBuilder builder = new DocumentBuilder();

for (int i = 0; i < 10000; i++)
{
    using (Bitmap bmp = new Bitmap(5, 5))
    using (Graphics g = Graphics.FromImage(bmp))
    {
        g.Clear(Color.FromArgb(random.Next(0, 254), random.Next(0, 254), random.Next(0, 254)));
        using (MemoryStream ms = new MemoryStream())
        {
            bmp.Save(ms, System.Drawing.Imaging.ImageFormat.Png);
            builder.InsertImage(ms.ToArray());
        }
    }
}

builder.Document.Save(ArtifactsDir + "OoxmlSaveOptions.Zip64ModeOption.docx", 
    new OoxmlSaveOptions { Zip64Mode = Zip64Mode.Always });
```

### Siehe auch

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
