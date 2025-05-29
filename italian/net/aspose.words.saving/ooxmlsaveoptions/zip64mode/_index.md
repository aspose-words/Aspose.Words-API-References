---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words per .NET
description: Scopri la proprietà Zip64Mode di OoxmlSaveOptions per migliorare l'output dei tuoi documenti in formato ZIP64. Ottimizza i file di grandi dimensioni senza sforzo!
type: docs
weight: 80
url: /it/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

Specifica se utilizzare o meno le estensioni del formato ZIP64 per il documento di output. Il valore predefinito èNever .

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

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

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
