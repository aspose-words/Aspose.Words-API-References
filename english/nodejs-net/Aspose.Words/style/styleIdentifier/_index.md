---
title: Style.styleIdentifier property
linktitle: styleIdentifier property
articleTitle: styleIdentifier property
second_title: Aspose.Words for NodeJs
description: "Style.styleIdentifier property. Gets the locale independent style identifier for a built-in style."
type: docs
weight: 180
url: /nodejs-net/aspose.words/style/styleIdentifier/
---

## Style.styleIdentifier property

Gets the locale independent style identifier for a built-in style.


```js
get styleIdentifier(): Aspose.Words.StyleIdentifier
```

### Remarks

For user defined (custom) styles, this property returns [StyleIdentifier.User](../../styleidentifier/#User).




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
* class [Style](../)
* property [Style.name](../name/)

