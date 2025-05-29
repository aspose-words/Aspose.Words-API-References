---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words per .NET
description: Scopri la proprietà DocumentSplitCriteria di HtmlSaveOptions per ottimizzare il salvataggio dei documenti nei formati HTML, EPUB e AZW3. Migliora il tuo controllo sulla formattazione oggi stesso!
type: docs
weight: 80
url: /it/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Specifica come il documento deve essere diviso durante il salvataggioHtml , Epub OAzw3 format. Il valore predefinito èNone per HTML e HeadingParagraph per EPUB e AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Osservazioni

Di solito si desidera salvare un documento in formato HTML come un singolo file. Ma in alcuni casi è preferibile suddividere l'output in diverse pagine HTML più piccole. Quando si salva in formato HTML, queste pagine verranno emesse in file o flussi individuali. Quando si salva in formato EPUB, verranno incorporate nei pacchetti corrispondenti.

Non è possibile dividere un documento quando lo si salva in formato MHTML.

## Esempi

Mostra come utilizzare una codifica specifica quando si salva un documento in formato .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilizzare un oggetto SaveOptions per specificare la codifica per un documento che salveremo.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Per impostazione predefinita, un documento .epub di output avrà tutto il suo contenuto in una parte HTML.
// Un criterio di suddivisione consente di segmentare il documento in più parti HTML.
// Imposteremo i criteri per suddividere il documento in paragrafi di intestazione.
// Questa funzione è utile per i lettori che non riescono a leggere file HTML di dimensioni superiori a una determinata soglia.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Specificare che si desidera esportare le proprietà del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Guarda anche

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
