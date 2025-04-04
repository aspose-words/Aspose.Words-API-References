---
title: TabStopCollection.getPositionByIndex method
linktitle: getPositionByIndex method
articleTitle: getPositionByIndex method
second_title: Aspose.Words for Node.js
description: "TabStopCollection.getPositionByIndex method. Gets the position (in points) of the tab stop at the specified index."
type: docs
weight: 100
url: /nodejs-net/aspose.words/tabstopcollection/getPositionByIndex/
---

## getPositionByIndex(index) {#number}

Gets the position (in points) of the tab stop at the specified index.


```js
getPositionByIndex(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | An index into the collection of tab stops. |

### Returns

The position of the tab stop.


### Examples

Shows how to find a tab, stop by its index and verify its position.

```js
let doc = new aw.Document();
let tabStops = doc.firstSection.body.paragraphs.at(0).paragraphFormat.tabStops;

tabStops.add(aw.ConvertUtil.millimeterToPoint(30), aw.TabAlignment.Left, aw.TabLeader.Dashes);
tabStops.add(aw.ConvertUtil.millimeterToPoint(60), aw.TabAlignment.Left, aw.TabLeader.Dashes);

// Verify the position of the second tab stop in the collection.
expect(tabStops.getPositionByIndex(1)).toBeCloseTo(aw.ConvertUtil.millimeterToPoint(60), 1);
```

### See Also

* module [Aspose.Words](../../)
* class [TabStopCollection](../)

