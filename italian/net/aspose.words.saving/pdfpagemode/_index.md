---
title: PdfPageMode Enum
linktitle: PdfPageMode
articleTitle: PdfPageMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.PdfPageMode per opzioni di visualizzazione PDF personalizzabili, migliorando l'esperienza utente in qualsiasi lettore PDF. Ottimizza i tuoi documenti oggi stesso!
type: docs
weight: 6300
url: /it/net/aspose.words.saving/pdfpagemode/
---
## PdfPageMode enumeration

Specifica come deve essere visualizzato il documento PDF quando viene aperto nel lettore PDF.

```csharp
public enum PdfPageMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseNone | `0` | Non sono visibili né il contorno del documento né le immagini in miniatura. |
| UseOutlines | `1` | Il contorno del documento è visibile. Nota che se nel documento PDF non sono presenti contorni, il riquadro di navigazione del contorno non sarà comunque visibile. |
| UseThumbs | `2` | Le immagini in miniatura sono visibili. |
| FullScreen | `3` | Modalità a schermo intero, senza barra dei menu, controlli delle finestre o altre finestre visibili. |
| UseOC | `4` | Il pannello del gruppo di contenuti opzionali è visibile. |
| UseAttachments | `5` | Il pannello Allegati è visibile. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
