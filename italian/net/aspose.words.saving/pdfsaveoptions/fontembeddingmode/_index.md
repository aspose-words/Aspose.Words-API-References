---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words per .NET
description: PdfSaveOptions FontEmbeddingMode proprietà. Specifica la modalità di incorporamento dei caratteri in C#.
type: docs
weight: 170
url: /it/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Specifica la modalità di incorporamento dei caratteri.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Osservazioni

Il valore predefinito èEmbedAll.

Questa impostazione funziona solo per il testo nella codifica ANSI (Windows-1252). Se il documento contiene testo non ANSI, i caratteri corrispondenti verranno incorporati indipendentemente da questa impostazione.

La conformità PDF/A e PDF/UA richiede che tutti i caratteri siano incorporati. EmbedAll il valore verrà utilizzato automaticamente durante il salvataggio in PDF/A e PDF/UA.

## Esempi

Mostra come impostare Aspose.Words per evitare di incorporare i caratteri Arial e Times New Roman in un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" è un carattere standard e "Courier New" è un carattere non standard.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "EmbedFullFonts" su "true" per incorporare ogni glifo di ogni carattere incorporato nel PDF di output.
options.EmbedFullFonts = true;

// Imposta la proprietà "FontEmbeddingMode" su "EmbedAll" per incorporare tutti i caratteri nel PDF di output.
// Imposta la proprietà "FontEmbeddingMode" su "EmbedNonstandard" per consentire solo l'incorporamento di caratteri non standard nel PDF di output.
// Imposta la proprietà "FontEmbeddingMode" su "EmbedNone" per non incorporare alcun carattere nel PDF di output.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);

switch (pdfFontEmbeddingMode)
{
    case PdfFontEmbeddingMode.EmbedAll:
        Assert.That(1000000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNonstandard:
        Assert.That(480000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNone:
        Assert.That(4255, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### Guarda anche

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
