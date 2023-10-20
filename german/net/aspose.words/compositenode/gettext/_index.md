---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words für .NET
description: CompositeNode GetText methode. Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab in C#.
type: docs
weight: 110
url: /de/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab.

```csharp
public override string GetText()
```

## Bemerkungen

Die zurückgegebene Zeichenfolge enthält alle Steuer- und Sonderzeichen, wie in beschrieben[`ControlChar`](../../controlchar/).

## Beispiele

Zeigt den Unterschied zwischen dem Aufruf der GetText- und ToString-Methoden auf einem Knoten.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText ruft den sichtbaren Text sowie Feldcodes und Sonderzeichen ab.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString gibt uns das Aussehen des Dokuments, wenn es in einem übergebenen Speicherformat gespeichert wird.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Zeigt, wie alle Absätze in einem Dokument ausgegeben werden, bei denen es sich um Listenelemente handelt.

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

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Siehe auch

* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
