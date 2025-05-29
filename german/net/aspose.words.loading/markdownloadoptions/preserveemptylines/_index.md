---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „MarkdownLoadOptions PreserveEmptyLines“ das Laden Ihres Markdown-Dokuments verbessert, indem leere Zeilen zur Verbesserung der Lesbarkeit beibehalten werden.
type: docs
weight: 30
url: /de/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

Ruft einen booleschen Wert ab oder setzt ihn, der angibt, ob leere Zeilen beim Laden einesMarkdown document. Der Standardwert ist`FALSCH` .

Normalerweise werden Leerzeilen zwischen Blockelementen in Markdown ignoriert. Leerzeilen am Anfang und Ende des Dokuments werden ebenfalls ignoriert. Diese Option ermöglicht den Import solcher Leerzeilen.

```csharp
public bool PreserveEmptyLines { get; set; }
```

## Beispiele

Zeigt, wie beim Laden eines Dokuments leere Zeilen beibehalten werden.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Siehe auch

* class [MarkdownLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
