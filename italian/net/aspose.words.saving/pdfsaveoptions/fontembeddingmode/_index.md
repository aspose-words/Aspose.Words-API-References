---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontEmbeddingMode di PdfSaveOptions per ottimizzare l'incorporamento dei font nei tuoi PDF. Migliora la qualità e la compatibilità dei documenti senza sforzo!
type: docs
weight: 170
url: /it/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Specifica la modalità di incorporamento del font.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Osservazioni

Il valore predefinito èEmbedAll.

Questa impostazione funziona solo per il testo con codifica ANSI (Windows-1252). Se il documento contiene testo non ANSI, i font corrispondenti verranno incorporati indipendentemente da questa impostazione.

La conformità PDF/A e PDF/UA richiede che tutti i font siano incorporati. EmbedAll il valore verrà utilizzato automaticamente durante il salvataggio in formato PDF/A e PDF/UA.

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

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
