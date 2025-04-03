---
title: BuiltInDocumentProperties.hyperlinkBase property
linktitle: hyperlinkBase property
articleTitle: hyperlinkBase property
second_title: Aspose.Words for NodeJs
description: "BuiltInDocumentProperties.hyperlinkBase property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 110
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/hyperlinkBase/
---

## BuiltInDocumentProperties.hyperlinkBase property

Specifies the base string used for evaluating relative hyperlinks in this document.


```js
get hyperlinkBase(): string
```

### Remarks

Aspose.Words does not use this property.




### Examples

Shows how to store the base part of a hyperlink in the document's properties.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a relative hyperlink to a document in the local file system named "Document.docx".
// Clicking on the link in Microsoft Word will open the designated document, if it is available.
builder.insertHyperlink("Relative hyperlink", "Document.docx", false);

// This link is relative. If there is no "Document.docx" in the same folder
// as the document that contains this link, the link will be broken.
expect(fs.existsSync(base.artifactsDir + "Document.docx")).toEqual(false);
doc.save(base.artifactsDir + "DocumentProperties.hyperlinkBase.BrokenLink.docx");

// The document we are trying to link to is in a different directory to the one we are planning to save the document in.
// We could fix links like this by putting an absolute filename in each one. 
// Alternatively, we could provide a base link that every hyperlink with a relative filename
// will prepend to its link when we click on it. 
let properties = doc.builtInDocumentProperties;
properties.hyperlinkBase = base.myDir;

expect(fs.existsSync(properties.hyperlinkBase + doc.range.fields.at(0).asFieldHyperlink().address)).toEqual(true);

doc.save(base.artifactsDir + "DocumentProperties.hyperlinkBase.WorkingLink.docx");
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [BuiltInDocumentProperties](../)

