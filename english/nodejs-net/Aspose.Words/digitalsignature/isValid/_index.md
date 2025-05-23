﻿---
title: DigitalSignature.isValid property
linktitle: isValid property
articleTitle: isValid property
second_title: Aspose.Words for Node.js
description: "DigitalSignature.isValid property. Returns ``true`` if this digital signature is valid and the document has not been tampered with."
type: docs
weight: 30
url: /nodejs-net/aspose.words/digitalsignature/isValid/
---

## DigitalSignature.isValid property

Returns ``true`` if this digital signature is valid and the document has not been tampered with.



```js
get isValid(): boolean
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

