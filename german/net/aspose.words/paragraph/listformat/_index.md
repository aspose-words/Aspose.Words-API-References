---
title: Paragraph.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Paragraph ListFormat“, um einfach auf die Listenformatierung Ihres Absatzes zuzugreifen und diese anzupassen und so die Präsentation Ihres Dokuments zu verbessern.
type: docs
weight: 150
url: /de/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

Bietet Zugriff auf die Listenformatierungseigenschaften des Absatzes.

```csharp
public ListFormat ListFormat { get; }
```

## Beispiele

Zeigt, wie alle Absätze in einem Dokument ausgegeben werden, die Listenelemente sind.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Siehe auch

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
