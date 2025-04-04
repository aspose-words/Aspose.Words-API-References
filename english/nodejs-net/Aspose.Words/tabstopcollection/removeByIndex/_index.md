---
title: TabStopCollection.removeByIndex method
linktitle: removeByIndex method
articleTitle: removeByIndex method
second_title: Aspose.Words for Node.js
description: "TabStopCollection.removeByIndex method. Removes a tab stop at the specified index from the collection."
type: docs
weight: 110
url: /nodejs-net/aspose.words/tabstopcollection/removeByIndex/
---

## removeByIndex(index) {#number}

Removes a tab stop at the specified index from the collection.


```js
removeByIndex(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | An index into the collection of tab stops. |

### Examples

Shows how to select a tab stop in a document by its index and remove it.

```js
let doc = new aw.Document();
let tabStops = doc.firstSection.body.paragraphs.at(0).paragraphFormat.tabStops;

tabStops.add(aw.ConvertUtil.millimeterToPoint(30), aw.TabAlignment.Left, aw.TabLeader.Dashes);
tabStops.add(aw.ConvertUtil.millimeterToPoint(60), aw.TabAlignment.Left, aw.TabLeader.Dashes);

expect(tabStops.count).toEqual(2);

// Remove the first tab stop.
tabStops.removeByIndex(0);

expect(tabStops.count).toEqual(1);

doc.save(base.artifactsDir + "TabStopCollection.removeByIndex.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TabStopCollection](../)

