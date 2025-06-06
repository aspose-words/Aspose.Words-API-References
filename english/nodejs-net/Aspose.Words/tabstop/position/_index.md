﻿---
title: TabStop.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Node.js
description: "TabStop.position property. Gets the position of the tab stop in points."
type: docs
weight: 50
url: /nodejs-net/aspose.words/tabstop/position/
---

## TabStop.position property

Gets the position of the tab stop in points.


```js
get position(): number
```

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
* class [TabStop](../)

