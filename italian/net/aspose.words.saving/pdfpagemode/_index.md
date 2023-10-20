---
title: PdfPageMode Enum
linktitle: PdfPageMode
articleTitle: PdfPageMode
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.PdfPageMode enum. Specifica come deve essere visualizzato il documento PDF quando viene aperto nel lettore PDF in C#.
type: docs
weight: 5500
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
| UseNone | `0` | Non sono visibili né la struttura del documento né le immagini in miniatura. |
| UseOutlines | `1` | La struttura del documento è visibile. Tieni presente che se non sono presenti strutture nel documento PDF, il riquadro di navigazione della struttura non sarà comunque visibile. |
| UseThumbs | `2` | Le immagini in miniatura sono visibili. |
| FullScreen | `3` | Modalità a schermo intero, senza barra dei menu, controlli delle finestre o qualsiasi altra finestra visibile. |
| UseOC | `4` | Il pannello del gruppo di contenuti opzionale è visibile. |
| UseAttachments | `5` | Il pannello degli allegati è visibile. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
