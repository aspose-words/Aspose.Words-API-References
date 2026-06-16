---
title: StyleCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Node.js
description: "StyleCollection.add method. Creates a new user defined style and adds it the collection."
type: docs
weight: 80
url: /nodejs-net/aspose.words/stylecollection/add/
---

## add(type, name) {#styletype_string}

Creates a new user defined style and adds it the collection.


```js
add(type: Aspose.Words.StyleType, name: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [StyleType](../../styletype/) | A [StyleType](../../styletype/) value that specifies the type of the style to create. |
| name | string | Case sensitive name of the style to create. |

### Remarks

You can create character, paragraph or a list style.

When creating a list style, the style is created with default numbered list formatting (1 \\ a \\ i).

Throws an exception if a style with this name already exists.




### Examples

Shows how to create a list style and use it in a document.

```js
let doc = new aw.Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// We can contain an entire List object within a style.
let listStyle = doc.styles.add(aw.StyleType.List, "MyListStyle");

let list1 = listStyle.list;

expect(list1.isListStyleDefinition).toEqual(true);
expect(list1.isListStyleReference).toEqual(false);
expect(list1.isMultiLevel).toEqual(true);
expect(list1.style).toEqual(listStyle);

// Change the appearance of all list levels in our list.
for (let level of list1.listLevels)
{
  level.font.name = "Verdana";
  level.font.color = "#0000FF";
  level.font.bold = true;
}

let builder = new aw.DocumentBuilder(doc);

builder.writeln("Using list style first time:");

// Create another list from a list within a style.
let list2 = doc.lists.add(listStyle);

expect(list2.isListStyleDefinition).toEqual(false);
expect(list2.isListStyleReference).toEqual(true);
expect(list2.style).toEqual(listStyle);

// Add some list items that our list will format.
builder.listFormat.list = list2;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

builder.writeln("Using list style second time:");

// Create and apply another list based on the list style.
let list3 = doc.lists.add(listStyle);
builder.listFormat.list = list3;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

builder.document.save(base.artifactsDir + "Lists.CreateAndUseListStyle.docx");
```

Shows how to add a Style to a document's styles collection.

```js
let doc = new aw.Document();

let styles = doc.styles;
// Set default parameters for new styles that we may later add to this collection.
styles.defaultFont.name = "Courier New";
// If we add a style of the "StyleType.Paragraph", the collection will apply the values of
// its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
styles.defaultParagraphFormat.firstLineIndent = 15.0;
// Add a style, and then verify that it has the default settings.
styles.add(aw.StyleType.Paragraph, "MyStyle");

expect(styles.at(4).font.name).toEqual("Courier New");
expect(styles.at("MyStyle").paragraphFormat.firstLineIndent).toEqual(15.0);
```

### See Also

* module [Aspose.Words](../../)
* class [StyleCollection](../)

