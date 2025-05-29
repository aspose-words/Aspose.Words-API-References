---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.ColorMode per una resa cromatica ottimizzata. Migliora l'aspetto visivo del tuo documento con impostazioni colore precise.
type: docs
weight: 5600
url: /it/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Specifica come vengono resi i colori.

```csharp
public enum ColorMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Normal | `0` | Rendering con colori non modificati. |
| Grayscale | `1` | Rendering con colori in una gamma di tonalità di grigio dal bianco al nero. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
