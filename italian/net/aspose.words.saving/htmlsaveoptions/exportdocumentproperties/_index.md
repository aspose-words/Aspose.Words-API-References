---
title: HtmlSaveOptions.ExportDocumentProperties
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica se esportare le proprietà del documento integrate e personalizzate in HTML MHTML o EPUB. Il valore predefinito èfalso .
type: docs
weight: 130
url: /it/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Specifica se esportare le proprietà del documento integrate e personalizzate in HTML, MHTML o EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportDocumentProperties { get; set; }
```

### Esempi

Mostra come utilizzare una codifica specifica durante il salvataggio di un documento in .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Usa un oggetto SaveOptions per specificare la codifica per un documento che salveremo.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Per impostazione predefinita, un documento di output .epub avrà tutto il suo contenuto in una parte HTML.
// Un criterio diviso ci consente di segmentare il documento in più parti HTML.
// Definiremo i criteri per dividere il documento in paragrafi di intestazione.
// Questo è utile per i lettori che non possono leggere file HTML più significativi di una dimensione specifica.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Specifica che vogliamo esportare le proprietà del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


