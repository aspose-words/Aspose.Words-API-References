---
title: Enum WatermarkLayout
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.WatermarkLayout enum. Definisce il layout della filigrana rispetto al centro della filigrana.
type: docs
weight: 6370
url: /it/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Definisce il layout della filigrana rispetto al centro della filigrana.

```csharp
public enum WatermarkLayout
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Horizontal | `0` | Layout filigrana orizzontale. Corrisponde a 0 gradi di rotazione. |
| Diagonal | `315` | Layout filigrana diagonale. Corrisponde a 315 gradi di rotazione. |

### Esempi

Mostra come creare una filigrana di testo.

```csharp
Document doc = new Document();

// Aggiungi una filigrana di testo normale.
doc.Watermark.SetText("Aspose Watermark");

// Se desideriamo modificare la formattazione del testo usandola come filigrana,
// possiamo farlo passando un oggetto TextWatermarkOptions durante la creazione della filigrana.
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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


