---
title: Watermark.Remove
second_title: Aspose.Words per .NET API Reference
description: Watermark metodo. Rimuove la filigrana.
type: docs
weight: 20
url: /it/net/aspose.words/watermark/remove/
---
## Watermark.Remove method

Rimuove la filigrana.

```csharp
public void Remove()
```

### Esempi

Mostra come creare una filigrana di testo.

```csharp
Document doc = new Document();

// Aggiunge una filigrana di testo semplice.
doc.Watermark.SetText("Aspose Watermark");

// Se desideriamo modificare la formattazione del testo utilizzandolo come filigrana,
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

* class [Watermark](../)
* spazio dei nomi [Aspose.Words](../../watermark/)
* assemblea [Aspose.Words](../../../)


