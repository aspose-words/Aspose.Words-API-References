---
title: HtmlSaveOptions.Encoding
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica la codifica da utilizzare durante lesportazione in HTML MHTML o EPUB. Il valore predefinito ènuova codifica UTF8false UTF8 senza distinta base.
type: docs
weight: 100
url: /it/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

Specifica la codifica da utilizzare durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è`nuova codifica UTF8(false)` (UTF-8 senza distinta base).

```csharp
public Encoding Encoding { get; set; }
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


