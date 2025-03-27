---
title: TabStop class
linktitle: TabStop class
articleTitle: TabStop class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.TabStop class. Represents a single custom tab stop"
type: docs
weight: 1320
url: /nodejs-net/Aspose.Words/tabstop/
---

## TabStop class

Represents a single custom tab stop. The [TabStop](./) object is a member of the
[TabStopCollection](../tabstopcollection/) collection.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

Normally, a tab stop specifies a position where a tab stop exists. But because
tab stops can be inherited from parent styles, it might be needed for the child object
to define explicitly that there is no tab stop at a given position. To clear
an inherited tab stop at a given position, create a [TabStop](./) object and set
[TabStop.alignment](./alignment/) to [TabAlignment.Clear](../tabalignment/#Clear).

For more information see [TabStopCollection](../tabstopcollection/).




### Constructors
| Name | Description |
| --- | --- |
| [TabStop(position)](./TabStop/#number) | Initializes a new instance of this class. |
| [TabStop(position, alignment, leader)](./TabStop/#number_tabalignment_tableader) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [alignment](./alignment/) | Gets or sets the alignment of text at this tab stop. |
| [isClear](./isClear/) | Returns ``True`` if this tab stop clears any existing tab stops in this position. |
| [leader](./leader/) | Gets or sets the type of the leader line displayed under the tab character. |
| [position](./position/) | Gets the position of the tab stop in points. |

### Methods

| Name | Description |
| --- | --- |
|[ equals(rhs)](./equals/#tabstop) | Compares with the specified [TabStop](./). |

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

* module [Aspose.Words](../)
* class [ParagraphFormat](../paragraphformat/)
* class [TabStopCollection](../tabstopcollection/)
* property [Document.defaultTabStop](../document/defaultTabStop/)

