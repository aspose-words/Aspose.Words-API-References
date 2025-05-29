---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: .NET için Aspose.Words
description: Belgenizin çıktısını ZIP64 biçimiyle geliştirmek için OoxmlSaveOptions Zip64Mode özelliğini keşfedin. Büyük dosyaları zahmetsizce optimize edin!
type: docs
weight: 80
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

Çıktı belgesi için ZIP64 biçim uzantılarının kullanılıp kullanılmayacağını belirtir. Varsayılan değer:Never .

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

## Örnekler

ZIP64 format uzantılarının nasıl kullanılacağını gösterir.

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

### Ayrıca bakınız

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
