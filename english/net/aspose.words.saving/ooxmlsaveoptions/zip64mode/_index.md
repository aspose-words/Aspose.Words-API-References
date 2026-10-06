---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words for .NET
description: Discover the OoxmlSaveOptions Zip64Mode property to enhance your document's output with ZIP64 format. Optimize large files effortlessly!
type: docs
weight: 80
url: /net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

Specifies whether or not to use ZIP64 format extensions for the output document. The default value is Never.

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

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

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
