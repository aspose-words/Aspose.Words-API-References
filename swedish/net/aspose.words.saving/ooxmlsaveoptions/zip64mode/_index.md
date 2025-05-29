---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OoxmlSaveOptions Zip64Mode för att förbättra dokumentets utdata med ZIP64-format. Optimera stora filer utan ansträngning!
type: docs
weight: 80
url: /sv/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

Anger om ZIP64-formattillägg ska användas för utdatadokumentet. Standardvärdet ärNever .

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

## Exempel

Visar hur man använder ZIP64-formattillägg.

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

### Se även

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
