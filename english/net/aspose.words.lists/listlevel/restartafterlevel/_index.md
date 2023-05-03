---
title: ListLevel.RestartAfterLevel
linktitle: RestartAfterLevel
articleTitle: RestartAfterLevel
second_title: Aspose.Words for .NET API Reference
description: ListLevel RestartAfterLevel property. Sets or returns the list level that must appear before the specified list level restarts numbering in C#.
type: docs
weight: 100
url: /net/aspose.words.lists/listlevel/restartafterlevel/
---
## ListLevel.RestartAfterLevel property

Sets or returns the list level that must appear before the specified list level restarts numbering.

```csharp
public int RestartAfterLevel { get; set; }
```

## Remarks

The value of -1 means the numbering will continue.

## Examples

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
* namespace [Aspose.Words.Lists](../../listlevel/)
* assembly [Aspose.Words](../../../)
