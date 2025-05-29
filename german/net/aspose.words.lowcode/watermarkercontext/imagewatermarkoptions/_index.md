---
title: WatermarkerContext.ImageWatermarkOptions
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie mit WatermarkerContext anpassbare Textwasserzeichenoptionen, um Ihre Bilder zu verbessern und die Identität Ihrer Marke effektiv zu schützen.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/
---
## WatermarkerContext.ImageWatermarkOptions property

Optionen für das Textwasserzeichen.

```csharp
public ImageWatermarkOptions ImageWatermarkOptions { get; }
```

## Beispiele

Zeigt, wie mithilfe des Kontexts ein Wasserzeichenbild in das Dokument eingefügt wird.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

watermarkerContext.ImageWatermarkOptions.Scale = 50;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextImage.docx")
    .Execute();
```

Zeigt, wie mithilfe des Kontexts ein Wasserzeichenbild aus einem Stream in das Dokument eingefügt wird.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

    watermarkerContext.ImageWatermarkOptions.Scale = 50;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextImageStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Siehe auch

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [WatermarkerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
