---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.PdfFontEmbeddingMode per un'integrazione ottimale dei font nei PDF. Migliora la qualità dei documenti e garantisci una visualizzazione coerente del testo.
type: docs
weight: 6260
url: /it/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

Specifica come Aspose.Words dovrebbe incorporare i font.

```csharp
public enum PdfFontEmbeddingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words incorpora tutti i font. |
| EmbedNonstandard | `1` | Aspose.Words incorpora tutti i font, ad eccezione dei font standard di Windows Arial e Times New Roman. In questa modalità sono interessati solo i font Arial e Times New Roman perché MS Word non incorpora solo questi font quando salva un documento in PDF. |
| EmbedNone | `2` | Aspose.Words non incorpora alcun font. |

## Esempi

Mostra come impostare Aspose.Words in modo che salti l'incorporamento dei font Arial e Times New Roman in un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" è un font standard, mentre "Courier New" è un font non standard.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Impostare la proprietà "EmbedFullFonts" su "true" per incorporare ogni glifo di ogni font incorporato nel PDF di output.
options.EmbedFullFonts = true;
// Impostare la proprietà "FontEmbeddingMode" su "EmbedAll" per incorporare tutti i font nel PDF di output.
// Impostare la proprietà "FontEmbeddingMode" su "EmbedNonstandard" per consentire solo l'incorporamento di font non standard nel PDF di output.
// Impostare la proprietà "FontEmbeddingMode" su "EmbedNone" per non incorporare alcun font nel PDF di output.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
