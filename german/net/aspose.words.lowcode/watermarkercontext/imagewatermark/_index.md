---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie Ihre Bilder mit der WatermarkerContext ImageWatermark-Eigenschaft verbessern können, sodass Sie mühelos benutzerdefinierte Wasserzeichenbilder hinzufügen können.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

Als Wasserzeichen zu verwendende Bildbytes.

```csharp
public byte[] ImageWatermark { get; set; }
```

## Bemerkungen

Wenn beide`ImageWatermark` Und[`TextWatermark`](../textwatermark/) angegeben sind, überschreibt das Textwasserzeichen das Bildwasserzeichen.

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

* class [WatermarkerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
