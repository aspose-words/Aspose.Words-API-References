---
title: TextWatermarkOptions.Layout
linktitle: Layout
articleTitle: Layout
second_title: Aspose.Words per .NET
description: Scopri la proprietà Layout TextWatermarkOptions per personalizzare l'aspetto della tua filigrana. Impostala facilmente su Diagonal o sul tuo layout preferito per effetti visivi migliori.
type: docs
weight: 60
url: /it/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

Ottiene o imposta il layout della filigrana. Il valore predefinito èDiagonal .

```csharp
public WatermarkLayout Layout { get; set; }
```

## Esempi

Mostra come creare una filigrana di testo.

```csharp
Document doc = new Document();

// Aggiungi una filigrana di testo normale.
doc.Watermark.SetText("Aspose Watermark");

// Se desideriamo modificare la formattazione del testo utilizzandola come filigrana,
// Possiamo farlo passando un oggetto TextWatermarkOptions quando creiamo la filigrana.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Possiamo rimuovere una filigrana da un documento come questo.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Guarda anche

* enum [WatermarkLayout](../../watermarklayout/)
* class [TextWatermarkOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
