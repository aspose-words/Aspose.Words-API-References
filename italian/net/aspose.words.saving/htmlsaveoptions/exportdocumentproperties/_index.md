---
title: HtmlSaveOptions.ExportDocumentProperties
linktitle: ExportDocumentProperties
articleTitle: ExportDocumentProperties
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportDocumentProperties proprietà. Specifica se esportare le proprietà del documento integrate e personalizzate in HTML MHTML o EPUB. Il valore predefinito èfalso  in C#.
type: docs
weight: 120
url: /it/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Specifica se esportare le proprietà del documento integrate e personalizzate in HTML, MHTML o EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportDocumentProperties { get; set; }
```

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

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
