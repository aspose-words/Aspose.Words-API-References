---
title: MarkdownSaveOptions.LinkExportMode
linktitle: LinkExportMode
articleTitle: LinkExportMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà LinkExportMode di MarkdownSaveOptions per controllare la formattazione dei link nei file di output. Ottimizza le esportazioni dei tuoi documenti senza sforzo!
type: docs
weight: 100
url: /it/net/aspose.words.saving/markdownsaveoptions/linkexportmode/
---
## MarkdownSaveOptions.LinkExportMode property

Specifica come i collegamenti verranno scritti nel file di output. Il valore predefinito èAuto .

```csharp
public MarkdownLinkExportMode LinkExportMode { get; set; }
```

## Esempi

Mostra come i collegamenti verranno scritti nel file .md.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// L'immagine verrà scritta come riferimento:
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// L'immagine verrà scritta in linea:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### Guarda anche

* enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
