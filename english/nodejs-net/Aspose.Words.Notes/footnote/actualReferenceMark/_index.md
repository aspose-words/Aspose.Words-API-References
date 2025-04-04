---
title: Footnote.actualReferenceMark property
linktitle: actualReferenceMark property
articleTitle: actualReferenceMark property
second_title: Aspose.Words for Node.js
description: "Footnote.actualReferenceMark property. Gets the actual text of the reference mark displayed in the document for this footnote."
type: docs
weight: 20
url: /nodejs-net/aspose.words.notes/footnote/actualReferenceMark/
---

## Footnote.actualReferenceMark property

Gets the actual text of the reference mark displayed in the document for this footnote.


```js
get actualReferenceMark(): string
```

### Remarks

To initially populate values of this property for all reference marks of the document, or to update
the values after changes in the document that might affect the reference marks, you must execute the
[Document.updateActualReferenceMarks()](../../../aspose.words/document/updateActualReferenceMarks/#default) method.
Updating fields ([Document.updateFields()](../../../aspose.words/document/updateFields/#default)) may also be necessary to get the correct result.



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

* module [Aspose.Words.Notes](../../)
* class [Footnote](../)

