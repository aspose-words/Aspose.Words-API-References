---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Lists.ListFormat class. Allows to control what list formatting is applied to a paragraph in C#.
type: docs
weight: 3480
url: /net/aspose.words.lists/listformat/
---
## ListFormat class

Allows to control what list formatting is applied to a paragraph.

To learn more, visit the [Working with Lists](https://docs.aspose.com/words/net/working-with-lists/) documentation article.

```csharp
public class ListFormat
```

## Properties

| Name | Description |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | True when the paragraph has bulleted or numbered formatting applied to it. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Gets or sets the list this paragraph is a member of. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Returns the list level formatting plus any formatting overrides applied to the current paragraph. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Gets or sets the list level number (0 to 8) for the paragraph. |

## Methods

| Name | Description |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Starts a new default bulleted list and applies it to the paragraph. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Starts a new default numbered list and applies it to the paragraph. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Increases the list level of the current paragraph by one level. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Decreases the list level of the current paragraph by one level. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Removes numbers or bullets from the current paragraph and sets list level to zero. |

## Remarks

A paragraph in a Microsoft Word document can be bulleted or numbered. When a paragraph is bulleted or numbered, it is said that list formatting is applied to the paragraph.

You do not create objects of the `ListFormat` class directly. You access `ListFormat` as a property of another object that can have list formatting associated with it. At the moment the objects that can have list formatting are: [`Paragraph`](../../aspose.words/paragraph/), [`Style`](../../aspose.words/style/) and [`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` of a [`Paragraph`](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

`ListFormat` of a [`Style`](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

`ListFormat` of a [`DocumentBuilder`](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [`DocumentBuilder`](../../aspose.words/documentbuilder/).

The list formatting itself is stored inside a [`List`](../list/) object that is stored separately from the paragraphs. The list objects are stored inside a [`ListCollection`](../listcollection/) collection. There is a single [`ListCollection`](../listcollection/) collection per [`Document`](../../aspose.words/document/).

The paragraphs do not physically belong to a list. The paragraphs just reference a particular list object via the [`List`](./list/) property and a particular level in the list via the [`ListLevelNumber`](./listlevelnumber/) property. By setting these two properties you control what bullets and numbering is applied to a paragraph.

## Examples

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
