---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.Zip64Mode enum for efficient ZIP64 format use in OOXML files, enhancing file size management and compatibility.
type: docs
weight: 6680
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
    using (SKBitmap bmp = new SKBitmap(5, 5))
    using (SKCanvas canvas = new SKCanvas(bmp))
    {
        canvas.Clear(new SKColor((byte)random.Next(0, 254), (byte)random.Next(0, 254), (byte)random.Next(0, 254)));
        using (SKData data = bmp.Encode(SKEncodedImageFormat.Png, 100))
            builder.InsertImage(data.ToArray());
    }
}
OoxmlSaveOptions saveOptions =  new OoxmlSaveOptions { Zip64Mode = Zip64Mode.Always };
builder.Document.Save(ArtifactsDir + "OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
```

### See Also

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
