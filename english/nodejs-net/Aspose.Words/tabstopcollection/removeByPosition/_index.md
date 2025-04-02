---
title: TabStopCollection.removeByPosition method
linktitle: removeByPosition method
articleTitle: removeByPosition method
second_title: Aspose.Words for NodeJs
description: "TabStopCollection.removeByPosition method. Removes a tab stop at the specified position from the collection."
type: docs
weight: 120
url: /nodejs-net/Aspose.Words/tabstopcollection/removeByPosition/
---

## removeByPosition(position) {#number}

Removes a tab stop at the specified position from the collection.


```js
removeByPosition(position: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | number | The position (in points) of the tab stop to remove. |

### Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```js
let doc = new aw.Document(base.myDir + "Table of contents.docx");

// Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
for (var paraNode of doc.getChildNodes(aw.NodeType.Paragraph, true)) {
  var para = paraNode.asParagraph();
  if (para.paragraphFormat.style.styleIdentifier >= aw.StyleIdentifier.Toc1 &&
    para.paragraphFormat.style.styleIdentifier <= aw.StyleIdentifier.Toc9)
  {
    // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
    let tab = para.paragraphFormat.tabStops.at(0);

    // Replace the first default tab, stop with a custom tab stop.
    para.paragraphFormat.tabStops.removeByPosition(tab.position);
    para.paragraphFormat.tabStops.add(tab.position - 50, tab.alignment, tab.leader);
  }
}

doc.save(base.artifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TabStopCollection](../)

