---
title: HtmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà SaveFormat di HtmlSaveOptions per salvare facilmente i documenti nei formati Html, Mhtml, Epub, Azw3 o Mobi per un'accessibilità versatile.
type: docs
weight: 460
url: /it/net/aspose.words.saving/htmlsaveoptions/saveformat/
---
## HtmlSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essereHtml ,Mhtml ,Epub , Azw3 OMobi .

```csharp
public override SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
