---
title: DigitalSignature.signTime property
linktitle: signTime property
articleTitle: signTime property
second_title: Aspose.Words for Node.js
description: "DigitalSignature.signTime property. Gets the time the document was signed."
type: docs
weight: 50
url: /nodejs-net/aspose.words/digitalsignature/signTime/
---

## DigitalSignature.signTime property

Gets the time the document was signed.


```js
get signTime(): Date
```

### Examples

Shows how to validate and display information about each signature in a document.

```js
const doc = new aw.Document(base.myDir + "Digitally signed.docx");

for (var i = 0; i < doc.digitalSignatures.count; i++) {
  const signature = doc.digitalSignatures.at(i);
  console.log(`${signature.isValid ? "Valid" : "Invalid"} signature: `);
  console.log(`\tReason:\t${signature.comments}`);
  console.log(`\tType:\t${signature.signatureType}`);
  console.log(`\tSign time:\t${signature.signTime}`);
  console.log(`\r\n`);
}
```

### See Also

* module [Aspose.Words](../../)
* class [DigitalSignature](../)

