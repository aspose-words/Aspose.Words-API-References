---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.Zip64Mode enum för effektiv användning av ZIP64-format i OOXML-filer, vilket förbättrar filstorlekshantering och kompatibilitet.
type: docs
weight: 6550
url: /sv/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

Anger när ZIP64-formattillägg ska användas för OOXML-filer.

```csharp
public enum Zip64Mode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Never | `0` | Använd inte ZIP64-formattillägg. |
| IfNecessary | `1` | Använd vid behov ZIP64-formattillägg. |
| Always | `2` | Använd alltid ZIP64-formattillägg. |

## Anmärkningar

En OOXML-fil är ett ZIP-arkiv som har en gräns på 4 GB (2^32 byte) för okomprimerad filstorlek, komprimerad filstorlek och arkivets totala storlek, samt en gräns på 65 535 (2^16-1) filer i arkivet. ZIP64-formattillägg ökar gränserna till 2^64.

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

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
