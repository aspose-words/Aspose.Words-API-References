﻿---
title: TabAlignment enumeration
linktitle: TabAlignment enumeration
articleTitle: TabAlignment enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.TabAlignment enumeration. Specifies the alignment/type of a tab stop."
type: docs
weight: 1280
url: /nodejs-net/aspose.words/tabalignment/
---

## TabAlignment enumeration

Specifies the alignment/type of a tab stop.


### Members

| Name | Description |
| --- | --- |
| Left | Left-aligns the text after the tab stop. |
| Center | Centers the text around the tab stop. |
| Right | Right-aligns the text at the tab stop. |
| Decimal | Aligns the text at the decimal dot. |
| Bar | Draws a vertical bar at the tab stop position. |
| List | The tab is a delimiter between the number/bullet and text in a list item. |
| Clear | Clears any tab stop in this position. |

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

* module [Aspose.Words](../)

