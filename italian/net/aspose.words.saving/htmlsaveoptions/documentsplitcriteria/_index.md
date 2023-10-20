---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words per .NET
description: HtmlSaveOptions DocumentSplitCriteria proprietà. Specifica come deve essere diviso il documento durante il salvataggio inHtml  Epub OAzw3 formato. Limpostazione predefinita èNone per HTML e HeadingParagraph per EPUB e AZW3 in C#.
type: docs
weight: 80
url: /it/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Specifica come deve essere diviso il documento durante il salvataggio inHtml , Epub OAzw3 formato. L'impostazione predefinita èNone per HTML e HeadingParagraph per EPUB e AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Osservazioni

Normalmente vorresti che un documento fosse salvato in HTML come un singolo file. Ma in alcuni casi è preferibile suddividere l'output in più pagine HTML più piccole. Quando si salva in formato HTML, queste pagine verranno inviate a singoli file o flussi. Quando si salva in formato EPUB verranno incorporati nei pacchetti corrispondenti.

Non è possibile dividere un documento durante il salvataggio nel formato MHTML.

## Esempi

Mostra come utilizzare una codifica specifica quando si salva un documento in .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilizza un oggetto SaveOptions per specificare la codifica per un documento che salveremo.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Per impostazione predefinita, un documento .epub di output avrà tutto il suo contenuto in una parte HTML.
// Un criterio di suddivisione ci permette di segmentare il documento in più parti HTML.
// Imposteremo i criteri per suddividere il documento in paragrafi di intestazione.
// Ciò è utile per i lettori che non possono leggere file HTML più significativi di una dimensione specifica.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Specifica che vogliamo esportare le proprietà del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Guarda anche

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
