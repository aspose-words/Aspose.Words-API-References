---
title: TabStopCollection.getIndexByPosition method
linktitle: getIndexByPosition method
articleTitle: getIndexByPosition method
second_title: Aspose.Words for NodeJs
description: "TabStopCollection.getIndexByPosition method. Gets the index of a tab stop with the specified position in points."
type: docs
weight: 90
url: /nodejs-net/aspose.words/tabstopcollection/getIndexByPosition/
---

## getIndexByPosition(position) {#number}

Gets the index of a tab stop with the specified position in points.


```js
getIndexByPosition(position: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | number |  |

### Examples

Shows how to look up a position to see if a tab stop exists there and obtain its index.

```js
let doc = new aw.Document();
let tabStops = doc.firstSection.body.paragraphs.at(0).paragraphFormat.tabStops;

// Add a tab stop at a position of 30mm.
tabStops.add(aw.ConvertUtil.millimeterToPoint(30), aw.TabAlignment.Left, aw.TabLeader.Dashes);

// A result of "0" returned by "GetIndexByPosition" confirms that a tab stop
// at 30mm exists in this collection, and it is at index 0.
expect(tabStops.getIndexByPosition(aw.ConvertUtil.millimeterToPoint(30))).toEqual(0);

// A "-1" returned by "GetIndexByPosition" confirms that
// there is no tab stop in this collection with a position of 60mm.
expect(tabStops.getIndexByPosition(aw.ConvertUtil.millimeterToPoint(60))).toEqual(-1);
```

### See Also

* module [Aspose.Words](../../)
* class [TabStopCollection](../)

