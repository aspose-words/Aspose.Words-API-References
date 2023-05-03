---
title: ListFormat.ListOutdent
linktitle: ListOutdent
articleTitle: ListOutdent
second_title: Aspose.Words for .NET API Reference
description: ListFormat ListOutdent method. Decreases the list level of the current paragraph by one level in C#.
type: docs
weight: 80
url: /net/aspose.words.lists/listformat/listoutdent/
---
## ListFormat.ListOutdent method

Decreases the list level of the current paragraph by one level.

```csharp
public void ListOutdent()
```

## Remarks

This method changes the list level and applies formatting properties of the new level.

In Word documents, lists may consist of up to nine levels. List formatting for each level specifies what bullet or number is used, left indent, space between the bullet and text etc.

## Examples

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

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Call the "ListIndent" method to increase the current list level,
// which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// These are the first three list items of the second list level, which will maintain a count
// independent of the count of the first list level. According to the current list format,
// they will have symbols of "a.", "b.", and "c.".
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Call the "ListOutdent" method to return to the previous list level.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

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
* namespace [Aspose.Words.Lists](../../listformat/)
* assembly [Aspose.Words](../../../)
