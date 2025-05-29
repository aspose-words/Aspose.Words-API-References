---
title: WatermarkerContext.TextWatermark
linktitle: TextWatermark
articleTitle: TextWatermark
second_title: Aspose.Words per .NET
description: Scopri la funzionalità WatermarkerContext TextWatermark per aggiungere facilmente filigrane di testo personalizzabili, migliorando la sicurezza e il branding dei tuoi contenuti.
type: docs
weight: 40
url: /it/net/aspose.words.lowcode/watermarkercontext/textwatermark/
---
## WatermarkerContext.TextWatermark property

Testo da utilizzare come filigrana.

```csharp
public string TextWatermark { get; set; }
```

## Osservazioni

Se entrambi[`ImageWatermark`](../imagewatermark/) E`TextWatermark` se specificati, la filigrana del testo sovrascrive la filigrana dell'immagine.

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

* class [WatermarkerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
