---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words per .NET
description: Scopri come la proprietà DefaultBookmarksOutlineLevel migliora i tuoi documenti Word ottimizzando la visibilità dei segnalibri nella struttura. Aumenta la produttività oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Specifica il livello predefinito nella struttura del documento in cui visualizzare i segnalibri di Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Osservazioni

Il livello dei singoli segnalibri può essere specificato utilizzando[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) proprietà.

Specificando 0, i segnalibri di Word non verranno visualizzati nella struttura del documento. Specificando 1, i segnalibri di Word verranno visualizzati nella struttura del documento al livello 1; 2 per il livello 2 e così via.

Il valore predefinito è 0. L'intervallo valido è compreso tra 0 e 9.

## Esempi

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

* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
