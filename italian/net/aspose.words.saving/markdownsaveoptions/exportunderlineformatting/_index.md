---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportUnderlineFormatting di MarkdownSaveOptions migliora l'esportazione del testo. Controlla facilmente la formattazione della sottolineatura con questa impostazione booleana.
type: docs
weight: 50
url: /it/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

Ottiene o imposta un valore booleano che indica di esportare la formattazione del testo sottolineato come sequenza di due caratteri più "++". Il valore predefinito è`falso` .

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## Esempi

Mostra come esportare la formattazione sottolineata come ++.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### Guarda anche

* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
