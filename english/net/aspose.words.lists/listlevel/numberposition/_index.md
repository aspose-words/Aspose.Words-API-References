---
title: ListLevel.NumberPosition
linktitle: NumberPosition
second_title: Aspose.Words for .NET API Reference
description: ListLevel NumberPosition property. Returns or sets the position in points of the number or bullet for the list level in C#.
type: docs
weight: 80
url: /net/aspose.words.lists/listlevel/numberposition/
---
## ListLevel.NumberPosition property

Returns or sets the position (in points) of the number or bullet for the list level.

```csharp
public double NumberPosition { get; set; }
```

## Remarks

`NumberPosition` corresponds to LeftIndent plus FirstLineIndent of the paragraph.

## Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```csharp
Document doc = new Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// This NumberFormat value will create star-shaped bullet list symbols.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Create paragraphs and apply both list levels of our custom list formatting to them.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### See Also

* class [ListLevel](../)
* namespace [Aspose.Words.Lists](../../listlevel/)
* assembly [Aspose.Words](../../../)
