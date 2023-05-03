---
title: CompositeNode.GetText
linktitle: GetText
second_title: Aspose.Words for .NET API Reference
description: CompositeNode GetText method. Gets the text of this node and of all its children in C#.
type: docs
weight: 120
url: /net/aspose.words/compositenode/gettext/
---
## GetText method

Gets the text of this node and of all its children.

```csharp
public override string GetText()
```

## Remarks

The returned string includes all control and special characters as described in [`ControlChar`](../../controlchar/).

## Examples

Shows the difference between calling the GetText and ToString methods on a node.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText will retrieve the visible text as well as field codes and special characters.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString will give us the document's appearance if saved to a passed save format.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Shows how to output all paragraphs in a document that are list items.

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

### See Also

* class [CompositeNode](../)
* namespace [Aspose.Words](../../compositenode/)
* assembly [Aspose.Words](../../../)
