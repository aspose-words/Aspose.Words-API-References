---
title: XpsSaveOptions.digitalSignatureDetails property
linktitle: digitalSignatureDetails property
articleTitle: digitalSignatureDetails property
second_title: Aspose.Words for Node.js
description: "XpsSaveOptions.digitalSignatureDetails property. Gets or sets [DigitalSignatureDetails](../../digitalsignaturedetails/) object used to sign a document."
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/xpssaveoptions/digitalSignatureDetails/
---

## XpsSaveOptions.digitalSignatureDetails property

Gets or sets [DigitalSignatureDetails](../../digitalsignaturedetails/) object used to sign a document.



```js
get digitalSignatureDetails(): Aspose.Words.Saving.DigitalSignatureDetails
```

### Examples

Shows how to sign XPS document.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");
let options = new aw.DigitalSignatures.SignOptions();
options.signTime = Date.now();
options.comments = "Some comments";

let digitalSignatureDetails = new aw.Saving.DigitalSignatureDetails(certificateHolder, options);

let saveOptions = new aw.Saving.XpsSaveOptions();
saveOptions.digitalSignatureDetails = digitalSignatureDetails;

expect(digitalSignatureDetails.certificateHolder).toEqual(certificateHolder);
expect(digitalSignatureDetails.signOptions.comments).toEqual("Some comments");

doc.save(base.artifactsDir + "XpsSaveOptions.XpsDigitalSignature.docx", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [XpsSaveOptions](../)

