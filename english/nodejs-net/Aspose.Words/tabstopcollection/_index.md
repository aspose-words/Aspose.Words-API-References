---
title: TabStopCollection class
linktitle: TabStopCollection class
articleTitle: TabStopCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.TabStopCollection class. A collection of [TabStop](../tabstop/) objects that represent custom tabs for a paragraph or a style"
type: docs
weight: 1330
url: /nodejs-net/aspose.words/tabstopcollection/
---

## TabStopCollection class

A collection of [TabStop](../tabstop/) objects that represent custom tabs for a paragraph or a style.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

In Microsoft Word documents, a tab stop can be defined in the properties of a paragraph
style or directly in the properties of a paragraph. A style can be based on another style.
Therefore, the complete set of tab stops for a given object is a combination of tab stops
defined directly on this object and tab stops inherited from the parent styles.

In Aspose.Words, when you obtain a [TabStopCollection](./) for a paragraph or a style,
it contains only the custom tab stops defined directly for this paragraph or style.
The collection does not include tab stops defined in the parent styles or default tab stops.




**Inheritance:** [TabStopCollection](./) → [InternableComplexAttr](../internablecomplexattr/)

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of tab stops in the collection. |
| [this[]](./this[]/) |  |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(tabStop)](./add/#tabstop) | Adds or replaces a tab stop in the collection. |
|[ add(position, alignment, leader)](./add/#number_tabalignment_tableader) | Adds or replaces a tab stop in the collection. |
|[ after(position)](./after/#number) | Gets a first tab stop to the right of the specified position. |
|[ before(position)](./before/#number) | Gets a first tab stop to the left of the specified position. |
|[ clear()](./clear/#default) | Deletes all tab stop positions. |
|[ equals(rhs)](./equals/#tabstopcollection) | Determines whether the specified [TabStopCollection](./) is equal in value to the current [TabStopCollection](./). |
|[ getIndexByPosition(position)](./getIndexByPosition/#number) | Gets the index of a tab stop with the specified position in points. |
|[ getPositionByIndex(index)](./getPositionByIndex/#number) | Gets the position (in points) of the tab stop at the specified index. |
|[ removeByIndex(index)](./removeByIndex/#number) | Removes a tab stop at the specified index from the collection. |
|[ removeByPosition(position)](./removeByPosition/#number) | Removes a tab stop at the specified position from the collection. |

### Examples

Shows how to work with a document's collection of tab stops.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let tabStops = builder.paragraphFormat.tabStops;

// 72 points is one "inch" on the Microsoft Word tab stop ruler.
tabStops.add(new aw.TabStop(72.0));
tabStops.add(new aw.TabStop(432.0, aw.TabAlignment.Right, aw.TabLeader.Dashes));

expect(tabStops.count).toEqual(2);
expect(tabStops.at(0).isClear).toEqual(false);
expect(tabStops.at(0).equals(tabStops.at(1))).toEqual(false);

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
builder.writeln("Start\tTab 1\tTab 2");

let paragraphs = doc.firstSection.body.paragraphs;

expect(paragraphs.count).toEqual(2);

// Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
expect(paragraphs.at(1).paragraphFormat.tabStops).toEqual(paragraphs.at(0).paragraphFormat.tabStops);

// A tab stop collection can point us to TabStops before and after certain positions.
expect(tabStops.before(100.0).position).toEqual(72.0);
expect(tabStops.after(100.0).position).toEqual(432.0);

// We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
paragraphs.at(1).paragraphFormat.tabStops.clear();

expect(paragraphs.at(1).paragraphFormat.tabStops.count).toEqual(0);

doc.save(base.artifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### See Also

* module [Aspose.Words](../)
* class [InternableComplexAttr](../internablecomplexattr/)
* class [ParagraphFormat](../paragraphformat/)
* class [TabStop](../tabstop/)
* property [Document.defaultTabStop](../document/defaultTabStop/)

