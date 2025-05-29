---
title: WatermarkerContext.TextWatermarkOptions
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words per .NET
description: Scopri le opzioni personalizzabili per le filigrane delle immagini con la proprietà WatermarkerContext TextWatermarkOptions per migliorare i tuoi elementi visivi e proteggere i tuoi contenuti.
type: docs
weight: 50
url: /it/net/aspose.words.lowcode/watermarkercontext/textwatermarkoptions/
---
## WatermarkerContext.TextWatermarkOptions property

Opzioni per la filigrana dell'immagine.

```csharp
public TextWatermarkOptions TextWatermarkOptions { get; }
```

## Esempi

Mostra come inserire il testo della filigrana nel documento utilizzando il contesto.

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

Mostra come inserire il testo della filigrana nel documento dal flusso utilizzando il contesto.

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

### Guarda anche

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [WatermarkerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
