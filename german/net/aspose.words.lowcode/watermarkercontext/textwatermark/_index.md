---
title: WatermarkerContext.TextWatermark
linktitle: TextWatermark
articleTitle: TextWatermark
second_title: Aspose.Words für .NET
description: Entdecken Sie die TextWatermark-Funktion von WatermarkerContext, mit der Sie ganz einfach anpassbare Textwasserzeichen hinzufügen und so die Sicherheit und das Branding Ihrer Inhalte verbessern können.
type: docs
weight: 40
url: /de/net/aspose.words.lowcode/watermarkercontext/textwatermark/
---
## WatermarkerContext.TextWatermark property

Als Wasserzeichen zu verwendender Text.

```csharp
public string TextWatermark { get; set; }
```

## Bemerkungen

Wenn beide[`ImageWatermark`](../imagewatermark/) Und`TextWatermark` angegeben sind, überschreibt das Textwasserzeichen das Bildwasserzeichen.

## Beispiele

Zeigt, wie mithilfe des Kontexts Wasserzeichentext in das Dokument eingefügt wird.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.TextWatermark = watermarkText;

watermarkerContext.TextWatermarkOptions.Color = Color.Red;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextText.docx")
    .Execute();
```

Zeigt, wie mithilfe des Kontexts Wasserzeichentext aus dem Stream in das Dokument eingefügt wird.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.TextWatermark = watermarkText;

    watermarkerContext.TextWatermarkOptions.Color = Color.Red;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextTextStream.docx", FileMode.Create, FileAccess.ReadWrite))
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
