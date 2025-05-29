---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: .NET için Aspose.Words
description: OOXML dosyalarında verimli ZIP64 formatı kullanımı, dosya boyutu yönetimi ve uyumluluğun iyileştirilmesi için Aspose.Words.Saving.Zip64Mode enum'unu keşfedin.
type: docs
weight: 6550
url: /tr/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

OOXML dosyaları için ZIP64 biçim uzantılarının ne zaman kullanılacağını belirtir.

```csharp
public enum Zip64Mode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Never | `0` | ZIP64 format uzantılarını kullanmayın. |
| IfNecessary | `1` | Gerekirse ZIP64 format uzantılarını kullanın. |
| Always | `2` | Her zaman ZIP64 format uzantılarını kullanın. |

## Notlar

OOXML dosyası, sıkıştırılmamış dosya boyutu, sıkıştırılmış dosya boyutu ve arşivin toplam boyutu için 4 GB (2^32 bayt) sınırı olan bir ZIP arşividir ve arşivde 65.535 (2^16-1) dosya sınırı vardır. ZIP64 biçim uzantıları sınırları 2^64'e çıkarır.

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

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
