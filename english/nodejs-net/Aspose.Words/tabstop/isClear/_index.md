---
title: TabStop.isClear property
linktitle: isClear property
articleTitle: isClear property
second_title: Aspose.Words for Node.js
description: "TabStop.isClear property. Returns ``true`` if this tab stop clears any existing tab stops in this position."
type: docs
weight: 30
url: /nodejs-net/aspose.words/tabstop/isClear/
---

## TabStop.isClear property

Returns ``true`` if this tab stop clears any existing tab stops in this position.



```js
get isClear(): boolean
```

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

* module [Aspose.Words](../../)
* class [TabStop](../)

