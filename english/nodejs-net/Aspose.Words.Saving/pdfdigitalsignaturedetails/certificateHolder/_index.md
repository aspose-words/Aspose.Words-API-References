﻿---
title: PdfDigitalSignatureDetails.certificateHolder property
linktitle: certificateHolder property
articleTitle: certificateHolder property
second_title: Aspose.Words for Node.js
description: "PdfDigitalSignatureDetails.certificateHolder property. Returns the certificate holder object that contains the certificate was used to sign the document."
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/pdfdigitalsignaturedetails/certificateHolder/
---

## PdfDigitalSignatureDetails.certificateHolder property

Returns the certificate holder object that contains the certificate was used to sign the document.


```js
get certificateHolder(): Aspose.Words.DigitalSignatures.CertificateHolder
```

### Examples

Shows how to sign a generated PDF document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Contents of signed PDF.");

let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
// digitally sign the document as we render it with the "Save" method.
let signingTime = new Date(2015, 7, 20);
options.digitalSignatureDetails =
  new aw.Saving.PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.digitalSignatureDetails.hashAlgorithm = aw.Saving.PdfDigitalSignatureHashAlgorithm.RipeMD160;

expect(options.digitalSignatureDetails.reason).toEqual("Test Signing");
expect(options.digitalSignatureDetails.location).toEqual("My Office");
//expect(options.digitalSignatureDetails.signatureDate).toEqual(signingTime);

doc.save(base.artifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfDigitalSignatureDetails](../)

