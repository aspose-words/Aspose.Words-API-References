---
title: ListFormat.isListItem property
linktitle: isListItem property
articleTitle: isListItem property
second_title: Aspose.Words for Node.js
description: "ListFormat.isListItem property. True when the paragraph has bulleted or numbered formatting applied to it."
type: docs
weight: 10
url: /nodejs-net/aspose.words.lists/listformat/isListItem/
---

## ListFormat.isListItem property

True when the paragraph has bulleted or numbered formatting applied to it.


```js
get isListItem(): boolean
```

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

Shows how to output all paragraphs in a document that are list items.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.listFormat.applyNumberDefault();
builder.writeln("Numbered list item 1");
builder.writeln("Numbered list item 2");
builder.writeln("Numbered list item 3");
builder.listFormat.removeNumbers();

builder.listFormat.applyBulletDefault();
builder.writeln("Bulleted list item 1");
builder.writeln("Bulleted list item 2");
builder.writeln("Bulleted list item 3");
builder.listFormat.removeNumbers();

let nodes = [...doc.getChildNodes(aw.NodeType.Paragraph, true)];

for (let node of nodes.filter(p => p.asParagraph().listFormat.isListItem))
{ 
  var para = node.asParagraph();
  console.log(`This paragraph belongs to list ID# ${para.listFormat.list.listId}, number style \"${para.listFormat.listLevel.numberStyle}\"`);
  console.log(`\t\"${para.getText().trim()}\"`);
}
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListFormat](../)

