---
title: Footnote constructor
linktitle: Footnote constructor
articleTitle: Footnote constructor
second_title: Aspose.Words for Node.js
description: "Footnote constructor. Initializes an instance of the [Footnote](../) class."
type: docs
weight: 10
url: /nodejs-net/aspose.words.notes/footnote/constructor/
---

## Footnote(doc, footnoteType) {#documentbase_footnotetype}

Initializes an instance of the [Footnote](../) class.



```js
Footnote(doc: Aspose.Words.DocumentBase, footnoteType: Aspose.Words.Notes.FootnoteType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |
| footnoteType | [FootnoteType](../../footnotetype/) | A [Footnote.footnoteType](../footnoteType/) value that specifies whether this is a footnote or endnote. |

### Remarks

When [Footnote](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parentNode](../../../aspose.words/node/parentNode/) is ``null``.

To append [Footnote](../) to the document use[CompositeNode.insertAfter()](../../../aspose.words/compositenode/insertAfter/#node_node) or [CompositeNode.insertBefore()](../../../aspose.words/compositenode/insertBefore/#node_node)
on the paragraph where you want the footnote inserted.




### See Also

* module [Aspose.Words.Notes](../../)
* class [Footnote](../)

