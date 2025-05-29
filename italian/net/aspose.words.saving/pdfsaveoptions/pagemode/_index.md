---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words per .NET
description: Scopri come la proprietà PageMode di PdfSaveOptions migliora la tua esperienza di visualizzazione dei PDF personalizzando la visualizzazione del documento in qualsiasi lettore PDF.
type: docs
weight: 260
url: /it/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Specifica come deve essere visualizzato il documento PDF quando viene aperto in un lettore PDF.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Osservazioni

Il valore predefinito èUseOutlines .

## Esempi

Mostra come impostare le istruzioni che alcuni lettori PDF devono seguire quando aprono un documento di output.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "PageMode" su "PdfPageMode.FullScreen" per far sì che il lettore PDF apra il file salvato
// documento in modalità a schermo intero, che occupa l'intera area di visualizzazione del monitor e non ha controlli visibili.
// Imposta la proprietà "PageMode" su "PdfPageMode.UseThumbs" per far sì che il lettore PDF visualizzi un pannello separato
// con una miniatura per ogni pagina del documento.
// Imposta la proprietà "PageMode" su "PdfPageMode.UseOC" per far sì che il lettore PDF visualizzi un pannello separato
// che ci consente di lavorare con tutti i livelli presenti nel documento.
// Imposta la proprietà "PageMode" su "PdfPageMode.UseOutlines" per ottenere il lettore PDF
// anche per visualizzare lo schema, se possibile.
// Impostare la proprietà "PageMode" su "PdfPageMode.UseNone" per far sì che il lettore PDF visualizzi solo il documento stesso.
// Impostare la proprietà "PageMode" su "PdfPageMode.UseAttachments" per rendere visibile il pannello degli allegati.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Mostra come elaborare i segnalibri nelle intestazioni e nei piè di pagina di un documento che stiamo convertendo in PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Impostare la proprietà "PageMode" su "PdfPageMode.UseOutlines" per visualizzare il riquadro di navigazione della struttura nel PDF di output.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Imposta la proprietà "DefaultBookmarksOutlineLevel" su "1" per visualizzare tutto
// segnalibri al primo livello della struttura nel PDF di output.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Imposta la proprietà "HeaderFooterBookmarksExportMode" su "HeaderFooterBookmarksExportMode.None" per
// non esportare alcun segnalibro presente nelle intestazioni/piè di pagina.
// Imposta la proprietà "HeaderFooterBookmarksExportMode" su "HeaderFooterBookmarksExportMode.First" per
// esportare i segnalibri solo nell'intestazione/piè di pagina della prima sezione.
// Imposta la proprietà "HeaderFooterBookmarksExportMode" su "HeaderFooterBookmarksExportMode.All" per
// esporta i segnalibri presenti in tutte le intestazioni/piè di pagina.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Guarda anche

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
