---
title: WatermarkerContext Class
linktitle: WatermarkerContext
articleTitle: WatermarkerContext
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.LowCode.WatermarkerContext per una filigrana impeccabile nei documenti. Migliora i tuoi documenti con facilità ed efficienza.
type: docs
weight: 4450
url: /it/net/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class

Contesto della filigrana del documento.

```csharp
public class WatermarkerContext : ProcessorContext
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [WatermarkerContext](watermarkercontext/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Impostazioni del font utilizzate dal processore. |
| [ImageWatermark](../../aspose.words.lowcode/watermarkercontext/imagewatermark/) { get; set; } | Byte dell'immagine da utilizzare come filigrana. |
| [ImageWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/) { get; } | Opzioni per la filigrana di testo. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opzioni di layout del documento utilizzate dal processore. |
| [TextWatermark](../../aspose.words.lowcode/watermarkercontext/textwatermark/) { get; set; } | Testo da utilizzare come filigrana. |
| [TextWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/textwatermarkoptions/) { get; } | Opzioni per la filigrana dell'immagine. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Callback di avviso utilizzato dal processore. |

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

Mostra come inserire un'immagine di filigrana nel documento utilizzando il contesto.

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

Mostra come inserire un'immagine di filigrana nel documento da un flusso utilizzando il contesto.

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

### Guarda anche

* class [ProcessorContext](../processorcontext/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
