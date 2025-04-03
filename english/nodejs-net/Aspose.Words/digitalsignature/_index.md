---
title: DigitalSignature class
linktitle: DigitalSignature class
articleTitle: DigitalSignature class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DigitalSignature class. Represents a digital signature on a document and the result of its verification"
type: docs
weight: 300
url: /nodejs-net/aspose.words/digitalsignature/
---

## DigitalSignature class

Represents a digital signature on a document and the result of its verification.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/nodejs-net/working-with-digital-signatures/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [certificateHolder](./certificateHolder/) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [comments](./comments/) | Gets the signing purpose comment. |
| [isValid](./isValid/) | Returns ``true`` if this digital signature is valid and the document has not been tampered with. |
| [issuerName](./issuerName/) | Returns the subject distinguished name of the certificate isuuer. |
| [signTime](./signTime/) | Gets the time the document was signed. |
| [signatureType](./signatureType/) | Gets the type of the digital signature. |
| [signatureValue](./signatureValue/) | Gets an array of bytes representing a signature value. |
| [subjectName](./subjectName/) | Returns the subject distinguished name of the certificate that was used to sign the document. |

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

* module [Aspose.Words](../)

