---
title: ListLevel.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words for .NET
description: Discover the ListLevel NumberFormat property to easily customize and set unique number formats for your lists, enhancing your document's clarity and style.
type: docs
weight: 70
url: /net/aspose.words.lists/listlevel/numberformat/
---
## ListLevel.NumberFormat property

Returns or sets the number format for the list level.

```csharp
public string NumberFormat { get; set; }
```

## Remarks

Among normal text characters, the string can contain placeholder characters \x0000 to \x0008 representing the numbers from the corresponding list levels.

For example, the string "\x0000.\x0001)" will generate a list label that looks something like "1.5)". The number "1" is the current number from the 1st list level, the number "5" is the current number from the 2nd list level.

Null is not allowed, but an empty string meaning no number is valid.

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

Shows advances ways of customizing list labels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
// These will look like "Appendix A", "Appendix B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
// If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Note that the higher-level uses UppercaseLetter numbering.
// We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
// These list labels will look like "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Make labels of all list levels bold.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Apply list formatting to the current paragraph.
builder.ListFormat.List = list;

// Create list items that will display all three of our list levels.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### See Also

* class [ListLevel](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
