---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImportUnderlineFormatting-Eigenschaft von MarkdownLoadOptions. Steuern Sie die Unterstreichungsformatierung mit einer einfachen booleschen Einstellung. Verbessern Sie Ihr Markdown-Erlebnis!
type: docs
weight: 20
url: /de/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob eine Sequenz von zwei Pluszeichen "++" als Unterstreichungstextformatierung erkannt werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## Beispiele

Zeigt, wie Pluszeichen „++“ als Unterstreichungstextformatierung erkannt werden.

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

### Siehe auch

* class [MarkdownLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
