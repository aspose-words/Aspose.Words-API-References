---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImportUnderlineFormatting di MarkdownLoadOptions. Controlla la formattazione del testo sottolineato con una semplice impostazione booleana. Migliora la tua esperienza di Markdown!
type: docs
weight: 20
url: /it/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

Ottiene o imposta un valore booleano che indica di riconoscere una sequenza di due caratteri più "++" come formattazione del testo sottolineato. Il valore predefinito è`falso` .

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## Esempi

Mostra come riconoscere i caratteri più "++" come formattazione del testo sottolineato.

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = true };
    Document doc = new Document(stream, loadOptions);

    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.Single, para.Runs[0].Font.Underline);

    loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = false };
    doc = new Document(stream, loadOptions);

    para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.None, para.Runs[0].Font.Underline);
}
```

### Guarda anche

* class [MarkdownLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
