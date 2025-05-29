---
title: HtmlSaveOptions.ExportDocumentProperties
linktitle: ExportDocumentProperties
articleTitle: ExportDocumentProperties
second_title: Aspose.Words per .NET
description: Scopri come ExportDocumentProperties di HtmlSaveOptions migliora le tue esportazioni HTML, MHTML o EPUB includendo proprietà essenziali del documento integrate e personalizzate.
type: docs
weight: 120
url: /it/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Specifica se esportare le proprietà del documento personalizzate e integrate in HTML, MHTML o EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportDocumentProperties { get; set; }
```

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

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
