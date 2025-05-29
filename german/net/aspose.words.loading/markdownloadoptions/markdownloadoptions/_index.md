---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den MarkdownLoadOptions-Konstruktor, um MarkdownLoadOptions-Instanzen für eine verbesserte Dokumentverarbeitung und -anpassung einfach zu initialisieren.
type: docs
weight: 10
url: /de/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

Initialisiert eine neue Instanz von[`MarkdownLoadOptions`](../) Klasse.

```csharp
public MarkdownLoadOptions()
```

## Bemerkungen

Setzt automatisch[`LoadFormat`](../../../aspose.words/loadformat/) ZuMarkdown .

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
