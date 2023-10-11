---
title: OutlineOptions.DefaultBookmarksOutlineLevel
second_title: Aspose.Words per .NET API Reference
description: OutlineOptions proprietà. Specifica il livello predefinito nella struttura del documento in cui visualizzare i segnalibri di Word.
type: docs
weight: 50
url: /it/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Specifica il livello predefinito nella struttura del documento in cui visualizzare i segnalibri di Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

### Osservazioni

È possibile specificare il livello dei singoli segnalibri utilizzando[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) proprietà.

Specifica 0 e i segnalibri di Word non verranno visualizzati nella struttura del documento. Specifica 1 e i segnalibri di Word verranno visualizzati nella struttura del documento al livello 1; 2 per il livello 2 e così via.

Il valore predefinito è 0. L'intervallo valido è compreso tra 0 e 9.

### Esempi

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

* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../outlineoptions/)
* assemblea [Aspose.Words](../../../)


