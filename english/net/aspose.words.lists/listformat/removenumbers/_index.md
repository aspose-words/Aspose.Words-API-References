---
title: ListFormat.RemoveNumbers
linktitle: RemoveNumbers
articleTitle: RemoveNumbers
second_title: Aspose.Words for .NET
description: Effortlessly remove numbers or bullets from your paragraphs with the ListFormat RemoveNumbers method, resetting your list level to zero for clean formatting.
type: docs
weight: 90
url: /net/aspose.words.lists/listformat/removenumbers/
---
## ListFormat.RemoveNumbers method

Removes numbers or bullets from the current paragraph and sets list level to zero.

```csharp
public void RemoveNumbers()
```

## Remarks

Calling this method is equivalent to setting the [`List`](../list/) property to `null`.

## Examples

Shows how to remove list formatting from all paragraphs in the main text of a section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);
Assert.That(paras.Count(n => ((Paragraph)n).ListFormat.IsListItem), Is.EqualTo(3));

foreach (Paragraph paragraph in paras)
    paragraph.ListFormat.RemoveNumbers();

Assert.That(paras.Count(n => ((Paragraph)n).ListFormat.IsListItem), Is.EqualTo(0));
```

Shows how to create bulleted and numbered lists.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create with a document builder.
// 1 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// End the bulleted list.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder.ListFormat.ApplyNumberDefault();

// This paragraph is the first item. The first item of a numbered list will have a "1." as its list item symbol.
builder.Writeln("Opening documents from different formats:");

Assert.That(builder.ListFormat.ListLevelNumber, Is.EqualTo(0));

// Call the "ListIndent" method to increase the current list level,
// which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
builder.ListFormat.ListIndent();

Assert.That(builder.ListFormat.ListLevelNumber, Is.EqualTo(1));

// These are the first three list items of the second list level, which will maintain a count
// independent of the count of the first list level. According to the current list format,
// they will have symbols of "a.", "b.", and "c.".
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Call the "ListOutdent" method to return to the previous list level.
builder.ListFormat.ListOutdent();

Assert.That(builder.ListFormat.ListLevelNumber, Is.EqualTo(0));

// These two paragraphs will continue the count of the first list level.
// These items will have symbols of "2.", and "3."
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// If we increase the list level to a level that we have added items to previously,
// the nested list will be separate from the previous, and its numbering will start from the beginning. 
// These list items will have symbols of "a.", "b.", "c.", "d.", and "e".
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Outdent the list level again.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// End the numbered list.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### See Also

* class [ListFormat](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
