---
title: Document.revisionsView property
linktitle: revisionsView property
articleTitle: revisionsView property
second_title: Aspose.Words for NodeJs
description: "Document.revisionsView property. Gets or sets a value indicating whether to work with the original or revised version of a document."
type: docs
weight: 360
url: /nodejs-net/aspose.words/document/revisionsView/
---

## Document.revisionsView property

Gets or sets a value indicating whether to work with the original or revised version of a document.


```js
get revisionsView(): Aspose.Words.RevisionsView
```

### Remarks

The default value is ****.



### Examples

Shows how to switch between the revised and the original view of a document.

```js
let doc = new aw.Document(base.myDir + "Revisions at list levels.docx");
doc.updateListLabels();

let paragraphs = doc.firstSection.body.paragraphs;
expect(paragraphs.at(0).listLabel.labelString).toEqual("1.");
expect(paragraphs.at(1).listLabel.labelString).toEqual("a.");
expect(paragraphs.at(2).listLabel.labelString).toEqual('');

// View the document object as if all the revisions are accepted. Currently supports list labels.
doc.revisionsView = aw.RevisionsView.Final;

expect(paragraphs.at(0).listLabel.labelString).toEqual('');
expect(paragraphs.at(1).listLabel.labelString).toEqual("1.");
expect(paragraphs.at(2).listLabel.labelString).toEqual("a.");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

