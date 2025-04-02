---
title: TabStopCollection.before method
linktitle: before method
articleTitle: before method
second_title: Aspose.Words for NodeJs
description: "TabStopCollection.before method. Gets a first tab stop to the left of the specified position."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words/tabstopcollection/before/
---

## before(position) {#number}

Gets a first tab stop to the left of the specified position.


```js
before(position: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | number | The reference position (in points). |

### Remarks

Skips tab stops with [TabStop.alignment](../../tabstop/alignment/) set to [TabAlignment.Bar](../../tabalignment/#Bar).




### Returns

A tab stop object or ``None`` if a suitable tab stop was not found.


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
* class [TabStopCollection](../)

