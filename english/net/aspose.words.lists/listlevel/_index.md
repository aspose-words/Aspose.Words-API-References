---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words for .NET
description: Aspose.Words.Lists.ListLevel class. Defines formatting for a list level in C#.
type: docs
weight: 3770
url: /net/aspose.words.lists/listlevel/
---
## ListLevel class

Defines formatting for a list level.

To learn more, visit the [Working with Lists](https://docs.aspose.com/words/net/working-with-lists/) documentation article.

```csharp
public class ListLevel
```

## Properties

| Name | Description |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Gets or sets the justification of the actual number of the list item. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; set; } | Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Specifies character formatting used for the list label. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Returns image data of the picture bullet shape for the current list level. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Gets or sets the paragraph style that is linked to this list level. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Returns or sets the number format for the list level. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Returns or sets the position (in points) of the number or bullet for the list level. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Returns or sets the number style for this list level. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Sets or returns the list level that must appear before the specified list level restarts numbering. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Returns or sets the starting number for this list level. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Returns or sets the tab position (in points) for the list level. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Returns or sets the position (in points) for the second line of wrapping text for the list level. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Returns or sets the character inserted after the number for the list level. |

## Methods

| Name | Description |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Creates picture bullet shape for the current list level. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Deletes picture bullet for the current list level. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | Compares with the specified ListLevel. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Calculates hash code for this object. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | Reports the string representation of the `ListLevel` object for the specified index of the list item. Parameters specify the [`NumberStyle`](../../aspose.words/numberstyle/) and an optional format string used when Custom is specified. |

## Remarks

You do not create objects of this class. List level objects are created automatically when a list is created. You access `ListLevel` objects via the [`ListLevelCollection`](../listlevelcollection/) collection.

Use the properties of `ListLevel` to specify list formatting for individual list levels.

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

* namespace [Aspose.Words.Lists](../../aspose.words.lists/)
* assembly [Aspose.Words](../../)
