---
title: Document.digitalSignatures property
linktitle: digitalSignatures property
articleTitle: digitalSignatures property
second_title: Aspose.Words for Node.js
description: "Document.digitalSignatures property. Gets the collection of digital signatures for this document and their validation results."
type: docs
weight: 110
url: /nodejs-net/aspose.words/document/digitalSignatures/
---

## Document.digitalSignatures property

Gets the collection of digital signatures for this document and their validation results.


```js
get digitalSignatures(): Aspose.Words.DigitalSignatures.DigitalSignatureCollection
```

### Remarks

This collection contains digital signatures that were loaded from the original document.
These digital signatures will not be saved when you save this [Document](../) object
into a file or stream because saving or converting will produce a document that is different from the
original and the original digital signatures will no longer be valid.

This collection is never ``null``. If the document is not signed, it will contain zero elements.




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
* class [Document](../)

