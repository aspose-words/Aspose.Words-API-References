---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.Zip64Mode enum. Specifies when to use ZIP64 format extensions for OOXML files in C#.
type: docs
weight: 6350
url: /net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

Specifies when to use ZIP64 format extensions for OOXML files.

```csharp
public enum Zip64Mode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Never | `0` | Do not use ZIP64 format extensions. |
| IfNecessary | `1` | If necessary use ZIP64 format extensions. |
| Always | `2` | Always use ZIP64 format extensions. |

## Remarks

OOXML file is a ZIP-archive that has a 4 GB (2^32 bytes) limit on uncompressed size of a file, compressed size of a file, and total size of the archive, as well as a limit of 65,535 (2^16-1) files in archive. ZIP64 format extensions increase the limits to 2^64.

## Examples

Shows how to use ZIP64 format extensions.

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

### See Also

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
