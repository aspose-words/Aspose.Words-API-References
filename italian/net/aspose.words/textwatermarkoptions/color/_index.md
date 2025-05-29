---
title: TextWatermarkOptions.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words per .NET
description: Personalizza le opzioni di TextWatermarkOptions con la proprietà Color per migliorarne la visibilità. Imposta il colore del carattere che preferisci per un tocco personalizzato. Il colore predefinito è Silver.
type: docs
weight: 20
url: /it/net/aspose.words/textwatermarkoptions/color/
---
## TextWatermarkOptions.Color property

Ottiene o imposta il colore del carattere. Il valore predefinito èSilver .

```csharp
public Color Color { get; set; }
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

* class [TextWatermarkOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
