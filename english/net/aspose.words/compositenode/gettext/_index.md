---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: CompositeNode GetText method. Gets the text of this node and of all its children in C#.
type: docs
weight: 130
url: /net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

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
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString will give us the document's appearance if saved to a passed save format.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
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

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### See Also

* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
