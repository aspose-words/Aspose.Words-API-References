---
title: ListLevelAlignment Enum
linktitle: ListLevelAlignment
articleTitle: ListLevelAlignment
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Lists.ListLevelAlignment enum for optimal list number and bullet alignment. Enhance document formatting effortlessly!
type: docs
weight: 3990
url: /net/aspose.words.lists/listlevelalignment/
---
## ListLevelAlignment enumeration

Specifies alignment for the list number or bullet.

```csharp
public enum ListLevelAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | `0` | The list label is aligned to the left of the number position. |
| Center | `1` | The list label is centered at the number position. |
| Right | `2` | This list label is aligned to the right of the number position. |

## Remarks

Used as a value for the [`Alignment`](../listlevel/alignment/) property.

## Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```csharp
Document doc = new Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
List docList = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = docList.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = docList.ListLevels[1];
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

builder.ListFormat.List = docList;
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

* namespace [Aspose.Words.Lists](../../aspose.words.lists/)
* assembly [Aspose.Words](../../)
