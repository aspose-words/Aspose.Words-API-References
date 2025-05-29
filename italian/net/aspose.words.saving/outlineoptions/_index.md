---
title: OutlineOptions Class
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.OutlineOptions per personalizzare le impostazioni della struttura del tuo documento, migliorando organizzazione e chiarezza.
type: docs
weight: 6140
url: /it/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

Consente di specificare le opzioni del contorno.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class OutlineOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [OutlineOptions](outlineoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | Consente di specificare il livello di struttura dei singoli segnalibri. |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | Ottiene o imposta un valore che determina se creare o meno livelli di struttura mancanti quando il documento viene esportato . |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | Specifica se creare o meno strutture per i titoli (paragrafi formattati con gli stili di titolo) all'interno delle tabelle. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | Specifica il livello predefinito nella struttura del documento in cui visualizzare i segnalibri di Word. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | Specifica quanti livelli nel documento devono essere visualizzati espansi quando il file viene visualizzato. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | Specifica quanti livelli di intestazioni (paragrafi formattati con gli stili di intestazione) includere nella struttura del documento . |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
