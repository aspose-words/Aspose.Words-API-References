---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà ColorMode di FixedPageSaveOptions per personalizzare la resa dei colori e migliorare la qualità dei documenti e l'impatto visivo. Ottimizza il tuo output oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Ottiene o imposta un valore che determina come vengono resi i colori.

```csharp
public ColorMode ColorMode { get; set; }
```

## Osservazioni

Il valore predefinito èNormal .

## Esempi

Mostra come modificare il colore dell'immagine con la proprietà delle opzioni di salvataggio.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
// Impostare la proprietà "ColorMode" su "Grayscale" per visualizzare tutte le immagini del documento in bianco e nero.
// Con questa impostazione la dimensione del documento di output potrebbe essere maggiore.
// Impostare la proprietà "ColorMode" su "Normale" per visualizzare tutte le immagini a colori.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Guarda anche

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
