---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.Zip64Mode per un utilizzo efficiente del formato ZIP64 nei file OOXML, migliorando la gestione delle dimensioni dei file e la compatibilità.
type: docs
weight: 6550
url: /it/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

Specifica quando utilizzare le estensioni del formato ZIP64 per i file OOXML.

```csharp
public enum Zip64Mode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Never | `0` | Non utilizzare le estensioni del formato ZIP64. |
| IfNecessary | `1` | Se necessario utilizzare le estensioni del formato ZIP64. |
| Always | `2` | Utilizzare sempre le estensioni del formato ZIP64. |

## Osservazioni

Il file OOXML è un archivio ZIP con un limite di 4 GB (2^32 byte) per la dimensione non compressa del file, la dimensione compressa del file e la dimensione totale dell'archivio, nonché un limite di 65.535 (2^16-1) file nell'archivio. Le estensioni del formato ZIP64 aumentano i limiti a 2^64.

## Esempi

Mostra come utilizzare le estensioni del formato ZIP64.

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

### Guarda anche

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
