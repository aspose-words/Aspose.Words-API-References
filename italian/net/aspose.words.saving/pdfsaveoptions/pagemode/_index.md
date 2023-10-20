---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words per .NET
description: PdfSaveOptions PageMode proprietà. Specifica come deve essere visualizzato il documento PDF quando viene aperto nel lettore PDF in C#.
type: docs
weight: 250
url: /it/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Specifica come deve essere visualizzato il documento PDF quando viene aperto nel lettore PDF.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Osservazioni

Il valore predefinito èUseOutlines .

## Esempi

Mostra come impostare le istruzioni da seguire per alcuni lettori PDF quando si apre un documento di output.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "PageMode" su "PdfPageMode.FullScreen" per fare in modo che il lettore PDF apra il file salvato
// documento in modalità a schermo intero, che assume il controllo della visualizzazione del monitor e non ha controlli visibili.
// Imposta la proprietà "PageMode" su "PdfPageMode.UseThumbs" per fare in modo che il lettore PDF visualizzi un pannello separato
// con una miniatura per ogni pagina del documento.
// Imposta la proprietà "PageMode" su "PdfPageMode.UseOC" per fare in modo che il lettore PDF visualizzi un pannello separato
// che ci permette di lavorare con tutti i livelli presenti nel documento.
// Imposta la proprietà "PageMode" su "PdfPageMode.UseOutlines" per ottenere il lettore PDF
// anche per visualizzare la struttura, se possibile.
// Imposta la proprietà "PageMode" su "PdfPageMode.UseNone" per fare in modo che il lettore PDF visualizzi solo il documento stesso.
// Imposta la proprietà "PageMode" su "PdfPageMode.UseAttachments" per rendere visibile il pannello degli allegati.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Mostra per elaborare i segnalibri nelle intestazioni/piè di pagina in un documento che stiamo convertendo in PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "PageMode" su "PdfPageMode.UseOutlines" per visualizzare il riquadro di navigazione della struttura nel PDF di output.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Imposta la proprietà "DefaultBookmarksOutlineLevel" su "1" per visualizzare tutto
// segnalibri al primo livello della struttura nel PDF di output.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Imposta la proprietà "HeaderFooterBookmarksExportMode" su "HeaderFooterBookmarksExportMode.None" su
// non esporta alcun segnalibro che si trova all'interno di intestazioni/piè di pagina.
// Imposta la proprietà "HeaderFooterBookmarksExportMode" su "HeaderFooterBookmarksExportMode.First" su
// esporta solo i segnalibri nell'intestazione/piè di pagina della prima sezione.
// Imposta la proprietà "HeaderFooterBookmarksExportMode" su "HeaderFooterBookmarksExportMode.All" su
// esporta i segnalibri che si trovano in tutte le intestazioni/piè di pagina.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Guarda anche

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
