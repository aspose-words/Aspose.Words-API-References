---
title: Enum ListTemplate
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Lists.ListTemplate enum. Specifies one of the predefined list formats available in Microsoft Word in C#
type: docs
weight: 3350
url: /net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Specifies one of the predefined list formats available in Microsoft Word.

```csharp
public enum ListTemplate
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| BulletDefault | `0` | Default bulleted list with 9 levels. Bullet of the first level is a disc, bullet of the second level is a circle, bullet of the third level is a square. Then formatting repeats for the remaining levels. |
| BulletDisk | `0` | Same as BulletDefault. |
| BulletCircle | `1` | The bullet of the first level is a circle. The remaining levels are same as in BulletDefault. |
| BulletSquare | `2` | The bullet of the first level is a square. The remaining levels are same as in BulletDefault. |
| BulletDiamonds | `3` | The bullet of the first level is a 4-diamond Wingding character. The remaining levels are same as in BulletDefault. |
| BulletArrowHead | `4` | The bullet of the first level is an arrow head Wingding character. The remaining levels are same as in BulletDefault. |
| BulletTick | `5` | The bullet of the first level is a tick Wingding character. The remaining levels are same as in BulletDefault. |
| NumberDefault | `6` | Default numbered list with 9 levels. Arabic numbering (1., 2., 3., ...) for the first level, lowercase letter numbering (a., b., c., ...) for the second level, lowercase roman numbering (i., ii., iii., ...) for the third level. Then formatting repeats for the remaining levels. |
| NumberArabicDot | `6` | Same as NumberDefault. |
| NumberArabicParenthesis | `7` | The number of the first level is "1)". The remaining levels are same as in NumberDefault. |
| NumberUppercaseRomanDot | `8` | The number of the first level is "I.". The remaining levels are same as in NumberDefault. |
| NumberUppercaseLetterDot | `9` | The number of the first level is "A.". The remaining levels are same as in NumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | The number of the first level is "a)". The remaining levels are same as in NumberDefault. |
| NumberLowercaseLetterDot | `11` | The number of the first level is "a.". The remaining levels are same as in NumberDefault. |
| NumberLowercaseRomanDot | `12` | The number of the first level is "i.". The remaining levels are same as in NumberDefault. |
| OutlineNumbers | `13` | An outline list with levels numbered "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | An outline list with levels are numbered "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | An outline lists with various bullets for different levels. |
| OutlineHeadingsArticleSection | `16` | An outline list with levels linked to Heading styles. |
| OutlineHeadingsLegal | `17` | An outline list with levels linked to Heading styles. |
| OutlineHeadingsNumbers | `18` | An outline list with levels linked to Heading styles. |
| OutlineHeadingsChapter | `19` | An outline list with levels linked to Heading styles. |

## Remarks

A list template value is used as a parameter into the [`Add`](../listcollection/add/) method.

Aspose.Words list templates correspond to the 21 list templates available in the Bullets and Numbering dialog box in Microsoft Word 2003.

## Examples

Shows how to create a document that contains all outline headings list templates.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

Shows how to restart numbering in a list by copying a list.

```csharp
Document doc = new Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize its first list level.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Apply our list to some paragraphs.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// We can add a copy of an existing list to the document's list collection
// to create a similar list without making changes to the original.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Apply the second list to new paragraphs.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Shows how to work with list levels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// By setting the "ListLevelNumber" property, we can increase the list level
// to begin a self-contained sub-list at the current list item.
// The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
// Deeper list levels use letters and lowercase Roman numerals. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
// Deeper levels of this list will use different symbols, such as "■" and "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### See Also

* namespace [Aspose.Words.Lists](../../aspose.words.lists/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
