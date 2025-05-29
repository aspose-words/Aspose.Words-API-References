---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words für .NET
description: Entdecken Sie die OoxmlSaveOptions Zip64Mode-Eigenschaft, um die Ausgabe Ihres Dokuments im ZIP64-Format zu verbessern. Optimieren Sie große Dateien mühelos!
type: docs
weight: 80
url: /de/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

Gibt an, ob ZIP64-Formaterweiterungen für das Ausgabedokument verwendet werden sollen. Der Standardwert istNever .

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

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

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
