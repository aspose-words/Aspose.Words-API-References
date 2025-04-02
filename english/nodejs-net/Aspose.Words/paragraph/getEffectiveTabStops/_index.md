---
title: Paragraph.getEffectiveTabStops method
linktitle: getEffectiveTabStops method
articleTitle: getEffectiveTabStops method
second_title: Aspose.Words for NodeJs
description: "Paragraph.getEffectiveTabStops method. Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists."
type: docs
weight: 270
url: /nodejs-net/Aspose.Words/paragraph/getEffectiveTabStops/
---

## getEffectiveTabStops() {#default}

Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists.


```js
getEffectiveTabStops()
```

### Examples

Shows how to set custom tab stops for a paragraph.

```js
let doc = new aw.Document();
let para = doc.firstSection.body.firstParagraph;

// If we are in a paragraph with no tab stops in this collection,
// the cursor will jump 36 points each time we press the Tab key in Microsoft Word.
expect(doc.firstSection.body.firstParagraph.getEffectiveTabStops().length).toEqual(0);

// We can add custom tab stops in Microsoft Word if we enable the ruler via the "View" tab.
// Each unit on this ruler is two default tab stops, which is 72 points.
// We can add custom tab stops programmatically like this.
let tabStops = doc.firstSection.body.firstParagraph.paragraphFormat.tabStops;
tabStops.add(72, aw.TabAlignment.Left, aw.TabLeader.Dots);
tabStops.add(216, aw.TabAlignment.Center, aw.TabLeader.Dashes);
tabStops.add(360, aw.TabAlignment.Right, aw.TabLeader.Line);

// We can see these tab stops in Microsoft Word by enabling the ruler via "View" -> "Show" -> "Ruler".
expect(para.getEffectiveTabStops().length).toEqual(3);

// Any tab characters we add will make use of the tab stops on the ruler and may,
// depending on the tab leader's value, leave a line between the tab departure and arrival destinations.
para.appendChild(new aw.Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.save(base.artifactsDir + "Paragraph.tabStops.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

