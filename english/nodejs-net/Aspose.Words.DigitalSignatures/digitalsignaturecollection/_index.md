---
title: DigitalSignatureCollection class
linktitle: DigitalSignatureCollection class
articleTitle: DigitalSignatureCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DigitalSignatures.DigitalSignatureCollection class. Provides a read-only collection of digital signatures attached to a document"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.DigitalSignatures/digitalsignaturecollection/
---

## DigitalSignatureCollection class

Provides a read-only collection of digital signatures attached to a document.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/nodejs-net/working-with-digital-signatures/) documentation article.




### Remarks

[Document.digitalSignatures](../../aspose.words/document/digitalSignatures/)



### Constructors
| Name | Description |
| --- | --- |
| [DigitalSignatureCollection()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |
| [isValid](./isValid/) | Returns ``true`` if all digital signatures in this collection are valid and the document has not been tampered with Also returns ``true`` if there are no digital signatures. Returns ``false`` if at least one digital signature is invalid. |
| [this[]](./this[]/) |  |

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

* module [Aspose.Words.DigitalSignatures](../)

