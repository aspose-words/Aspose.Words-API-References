---
title: Paragraph.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words for .NET
description: Discover the Paragraph ListFormat property to easily access and customize your paragraph's list formatting, enhancing your document's presentation.
type: docs
weight: 150
url: /net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

Provides access to the list formatting properties of the paragraph.

```csharp
public ListFormat ListFormat { get; }
```

## Examples

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

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
