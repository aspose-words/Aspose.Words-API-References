---
title: List Class
linktitle: List
articleTitle: List
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Lists.List class for powerful list formatting. Enhance your documents with seamless organization and professional presentation.
type: docs
weight: 3920
url: /net/aspose.words.lists/list/
---
## List class

Represents formatting of a list.

To learn more, visit the [Working with Lists](https://docs.aspose.com/words/net/working-with-lists/) documentation article.

```csharp
public class List : IComparable<List>
```

## Properties

| Name | Description |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Gets the owner document. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Returns `true` if this list is a definition of a list style. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Returns `true` if this list is a reference to a list style. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Returns `true` when the list contains 9 levels; `false` when 1 level. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Specifies whether list should be restarted at each section. Default value is `false`. |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Gets the unique identifier of the list. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Gets the collection of list levels for this list. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Gets the list style that this list references or defines. |

## Methods

| Name | Description |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(*List*) | Compares the specified list to the current list. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(*object*) | Compares the specified object to the current object. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(*List*) | Compares with the specified list. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(*object*) | Determines whether the specified object is equal in value to the current object. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Calculates hash code for this list object. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(*List*) | Returns true if the current list and the given list are created from the same template. |

## Remarks

A list in a Microsoft Word document is a set of list formatting properties. Each list can have up to 9 levels and formatting properties, such as number style, start value, indent, tab position etc are defined separately for each level.

A `List` object always belongs to the [`ListCollection`](../listcollection/) collection.

To create a new list, use the Add methods of the [`ListCollection`](../listcollection/) collection.

To modify formatting of a list, use [`ListLevel`](../listlevel/) objects found in the [`ListLevels`](./listlevels/) collection.

To apply or remove list formatting from a paragraph, use [`ListFormat`](../listformat/).

## Examples

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

Shows how to work with list levels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.That(builder.ListFormat.IsListItem, Is.False);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.That(builder.ListFormat.IsListItem, Is.True);

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

Assert.That(builder.ListFormat.IsListItem, Is.False);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### See Also

* namespace [Aspose.Words.Lists](../../aspose.words.lists/)
* assembly [Aspose.Words](../../)
