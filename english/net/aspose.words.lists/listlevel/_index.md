---
title: ListLevel
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 3240
url: /net/aspose.words.lists/listlevel/
---
## ListLevel class

Defines formatting for a list level.

```csharp
public class ListLevel
```

## Public Members

| Name | Description |
| --- | --- |
| [Alignment](alignment) { get; set; } | Gets or sets the justification of the actual number of the list item. |
| [CustomNumberStyleFormat](customnumberstyleformat) { get; } | Gets the custom number style format for this list level. For example: "a, ç, ĝ, ...". |
| [Font](font) { get; } | Specifies character formatting used for the list label. |
| [ImageData](imagedata) { get; } | Returns image data of the picture bullet shape for the current list level. |
| [IsLegal](islegal) { get; set; } | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [LinkedStyle](linkedstyle) { get; set; } | Gets or sets the paragraph style that is linked to this list level. |
| [NumberFormat](numberformat) { get; set; } | Returns or sets the number format for the list level. |
| [NumberPosition](numberposition) { get; set; } | Returns or sets the position (in points) of the number or bullet for the list level. |
| [NumberStyle](numberstyle) { get; set; } | Returns or sets the number style for this list level. |
| [RestartAfterLevel](restartafterlevel) { get; set; } | Sets or returns the list level that must appear before the specified list level restarts numbering. |
| [StartAt](startat) { get; set; } | Returns or sets the starting number for this list level. |
| [TabPosition](tabposition) { get; set; } | Returns or sets the tab position (in points) for the list level. |
| [TextPosition](textposition) { get; set; } | Returns or sets the position (in points) for the second line of wrapping text for the list level. |
| [TrailingCharacter](trailingcharacter) { get; set; } | Returns or sets the character inserted after the number for the list level. |
| [CreatePictureBullet](createpicturebullet)() | Creates picture bullet shape for the current list level. |
| [DeletePictureBullet](deletepicturebullet)() | Deletes picture bullet for the current list level. |
| [Equals](equals)(…) | Compares with the specified ListLevel. |
| override [GetHashCode](gethashcode)() | Calculates hash code for this object. |
| static [GetEffectiveValue](geteffectivevalue)(…) | Reports the string representation of the [`ListLevel`](../listlevel) object for the specified index of the list item. Parameters specify the [`NumberStyle`](../../aspose.words/numberstyle) and an optional format string used when Custom is specified. |

### Remarks

You do not create objects of this class. List level objects are created automatically when a list is created. You access [`ListLevel`](../listlevel) objects via the [`ListLevelCollection`](../listlevelcollection) collection.Use the properties of [`ListLevel`](../listlevel) to specify list formatting for individual list levels.

### Examples

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

* namespace [Aspose.Words.Lists](../../aspose.words.lists)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
