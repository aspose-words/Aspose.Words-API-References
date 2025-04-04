---
title: DigitalSignature.comments property
linktitle: comments property
articleTitle: comments property
second_title: Aspose.Words for Node.js
description: "DigitalSignature.comments property. Gets the signing purpose comment."
type: docs
weight: 20
url: /nodejs-net/aspose.words/digitalsignature/comments/
---

## DigitalSignature.comments property

Gets the signing purpose comment.


```js
get comments(): string
```

### Examples

Shows how to validate and display information about each signature in a document.

```js
const doc = new aw.Document(base.myDir + "Digitally signed.docx");

for (var i = 0; i < doc.digitalSignatures.count; i++) {
  const signature = doc.digitalSignatures.at(i);
  //console.log(`${signature.isValid ? "Valid" : "Invalid"} signature: `);
  //console.log(`\tReason:\t${signature.comments}`);
  //console.log(`\tType:\t${signature.signatureType}`);
  //console.log(`\tSign time:\t${signature.signTime}`);
  /*
  TODO: digitalSig.certificateHolder.certificate of X509Certificate2 type is not supported by Node.js.
  console.log(`\tSubject name:\t${signature.certificateHolder.certificate.subjectName}`);
  console.log(`\tIssuer name:\t${signature.certificateHolder.certificate.issuerName.name}`);
  */
  //console.log(`\r\n`);
}
```

### See Also

* module [Aspose.Words](../../)
* class [DigitalSignature](../)

