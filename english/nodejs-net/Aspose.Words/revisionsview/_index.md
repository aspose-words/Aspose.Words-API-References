---
title: RevisionsView enumeration
linktitle: RevisionsView enumeration
articleTitle: RevisionsView enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.RevisionsView enumeration. Allows to specify whether to work with the original or revised version of a document."
type: docs
weight: 1120
url: /nodejs-net/Aspose.Words/revisionsview/
---

## RevisionsView enumeration

Allows to specify whether to work with the original or revised version of a document.


### Members

| Name | Description |
| --- | --- |
| Original | Specifies original version of a document. |
| Final | Specifies revised version of a document. |

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

* module [Aspose.Words](../)

