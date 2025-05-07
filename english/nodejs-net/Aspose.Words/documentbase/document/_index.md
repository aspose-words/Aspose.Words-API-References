---
title: DocumentBase.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Node.js
description: "DocumentBase.document property. Gets this instance."
type: docs
weight: 20
url: /nodejs-net/aspose.words/documentbase/document/
---

## DocumentBase.document property

Gets this instance.


```js
get document(): Aspose.Words.DocumentBase
```

### Examples

Shows how to create simple document.

```js
const doc = new aw.Document();
// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
const section = new aw.Section(doc);
doc.appendChild(section);
const body = new aw.Body(doc);
section.appendChild(body);
const para = new aw.Paragraph(doc);
body.appendChild(para);
para.appendChild(new aw.Run(doc, "Hello world!"));
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBase](../)

