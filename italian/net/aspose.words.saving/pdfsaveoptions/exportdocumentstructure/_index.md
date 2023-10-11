---
title: PdfSaveOptions.ExportDocumentStructure
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Ottiene o imposta un valore che determina se esportare o meno la struttura del documento.
type: docs
weight: 140
url: /it/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Ottiene o imposta un valore che determina se esportare o meno la struttura del documento.

```csharp
public bool ExportDocumentStructure { get; set; }
```

### Osservazioni

Questo valore viene ignorato durante il salvataggio in PDF/A-1a, PDF/A-2a e PDF/UA-1 perché per questa conformità è richiesta la struttura del documento.

Tieni presente che l'esportazione della struttura del documento aumenta significativamente il consumo di memoria, soprattutto per i documenti di grandi dimensioni.

### Esempi

Mostra come preservare gli elementi della struttura del documento, che possono aiutare nell'interpretazione a livello di codice del nostro documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "ExportDocumentStructure" su "true" per rendere disponibile la struttura del documento, ad esempio i tag, tramite
// Pannello di navigazione "Contenuto" di Adobe Acrobat al costo di una maggiore dimensione del file.
// Imposta la proprietà "ExportDocumentStructure" su "false" per non esportare la struttura del documento.
options.ExportDocumentStructure = exportDocumentStructure;

// Supponiamo di esportare la struttura del documento durante il salvataggio di questo documento. In quel caso,
// possiamo aprirlo utilizzando Adobe Acrobat e trovare tag per elementi come l'intestazione
// e il paragrafo successivo tramite "Visualizza" -> "Mostra/Nascondi" -> "Riquadri di navigazione" -> "Tag".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


