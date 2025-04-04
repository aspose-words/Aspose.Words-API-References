---
title: Document.updateActualReferenceMarks method
linktitle: updateActualReferenceMarks method
articleTitle: updateActualReferenceMarks method
second_title: Aspose.Words for Node.js
description: "Document.updateActualReferenceMarks method. Updates the [Footnote.actualReferenceMark](../../../aspose.words.notes/footnote/actualReferenceMark/) property of all footnotes and endnotes in the document."
type: docs
weight: 750
url: /nodejs-net/aspose.words/document/updateActualReferenceMarks/
---

## updateActualReferenceMarks() {#default}

Updates the [Footnote.actualReferenceMark](../../../aspose.words.notes/footnote/actualReferenceMark/) property of all footnotes and endnotes in the document.



```js
updateActualReferenceMarks()
```

### Remarks

Updating fields ([Document.updateFields()](../updateFields/#default)) may be necessary to get the correct result.



### Examples

Shows how to get actual footnote reference mark.

```js
let doc = new aw.Document(base.myDir + "Footnotes and endnotes.docx");

let footnote = doc.getFootnote(1, true);
doc.updateFields();
doc.updateActualReferenceMarks();

expect(footnote.actualReferenceMark).toEqual("1");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

