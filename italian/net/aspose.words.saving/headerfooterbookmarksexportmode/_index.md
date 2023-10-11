---
title: Enum HeaderFooterBookmarksExportMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode enum. Specifica come vengono esportati i segnalibri nelle intestazioni/piè di pagina.
type: docs
weight: 5050
url: /it/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Specifica come vengono esportati i segnalibri nelle intestazioni/piè di pagina.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | I segnalibri nelle intestazioni/piè di pagina non vengono esportati. |
| First | `1` | Viene esportato solo il segnalibro nella prima intestazione/piè di pagina della sezione. |
| All | `2` | I segnalibri in tutte le intestazioni/piè di pagina vengono esportati. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


