---
title: ListFormat class
linktitle: ListFormat class
articleTitle: ListFormat class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Lists.ListFormat class. Allows to control what list formatting is applied to a paragraph"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Lists/listformat/
---

## ListFormat class

Allows to control what list formatting is applied to a paragraph.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/nodejs-net/working-with-lists/) documentation article.




### Remarks

A paragraph in a Microsoft Word document can be bulleted or numbered.
When a paragraph is bulleted or numbered, it is said that list formatting
is applied to the paragraph.

You do not create objects of the [ListFormat](./) class directly.
You access [ListFormat](./) as a property of another object that can
have list formatting associated with it. At the moment the objects that can
have list formatting are: [Paragraph](../../Aspose.Words/paragraph/),
[Style](../../Aspose.Words/style/) and [DocumentBuilder](../../Aspose.Words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../Aspose.Words/paragraph/) specifies
what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../Aspose.Words/style/) (applicable
to paragraph styles only) allows to specify what list formatting and list level
is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../Aspose.Words/documentbuilder/)
provides access to the list formatting at the current cursor position
inside the [DocumentBuilder](../../Aspose.Words/documentbuilder/).

The list formatting itself is stored inside a [List](../../Aspose.Words/list/)
object that is stored separately from the paragraphs. The list objects
are stored inside a [ListCollection](../listcollection/) collection. There is a single
[ListCollection](../listcollection/) collection per [Document](../../Aspose.Words/document/).

The paragraphs do not physically belong to a list. The paragraphs just
reference a particular list object via the [ListFormat.list](./list/) property
and a particular level in the list via the [ListFormat.listLevelNumber](./listLevelNumber/) property.
By setting these two properties you control what bullets and numbering is
applied to a paragraph.




### Properties

| Name | Description |
| --- | --- |
| [isListItem](./isListItem/) | True when the paragraph has bulleted or numbered formatting applied to it. |
| [list](./list/) | Gets or sets the list this paragraph is a member of. |
| [listLevel](./listLevel/) | Returns the list level formatting plus any formatting overrides applied to the current paragraph. |
| [listLevelNumber](./listLevelNumber/) | Gets or sets the list level number (0 to 8) for the paragraph. |

### Methods

| Name | Description |
| --- | --- |
|[ applyBulletDefault()](./applyBulletDefault/#default) | Starts a new default bulleted list and applies it to the paragraph. |
|[ applyNumberDefault()](./applyNumberDefault/#default) | Starts a new default numbered list and applies it to the paragraph. |
|[ listIndent()](./listIndent/#default) | Increases the list level of the current paragraph by one level. |
|[ listOutdent()](./listOutdent/#default) | Decreases the list level of the current paragraph by one level. |
|[ removeNumbers()](./removeNumbers/#default) | Removes numbers or bullets from the current paragraph and sets list level to zero. |

### Examples

Shows how to work with list levels.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

expect(builder.listFormat.isListItem).toEqual(false);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.NumberDefault);

expect(builder.listFormat.isListItem).toEqual(true);

// By setting the "ListLevelNumber" property, we can increase the list level
// to begin a self-contained sub-list at the current list item.
// The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
// Deeper list levels use letters and lowercase Roman numerals. 
for (let i = 0; i < 9; i++)
{
  builder.listFormat.listLevelNumber = i;
  builder.writeln("Level " + i);
}

// 2 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
// Deeper levels of this list will use different symbols, such as "■" and "○".
builder.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.BulletDefault);

for (let i = 0; i < 9; i++)
{
  builder.listFormat.listLevelNumber = i;
  builder.writeln("Level " + i);
}

// We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder.listFormat.list = null;

expect(builder.listFormat.isListItem).toEqual(false);

doc.save(base.artifactsDir + "Lists.SpecifyListLevel.docx");
```

### See Also

* module [Aspose.Words.Lists](../)

