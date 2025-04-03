---
title: SignOptions.signatureLineId property
linktitle: signatureLineId property
articleTitle: signatureLineId property
second_title: Aspose.Words for NodeJs
description: "SignOptions.signatureLineId property. Signature line identifier"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.DigitalSignatures/signoptions/signatureLineId/
---

## SignOptions.signatureLineId property

Signature line identifier.
Default value is **Empty (all zeroes) Guid**.



```js
get signatureLineId(): uuid
```

### Remarks

When set, it associates [SignatureLine](../../../aspose.words.drawing/signatureline/) with corresponding [DigitalSignature](../../../aspose.words/digitalsignature/).



### Examples

Shows how to add a signature line to a document, and then sign it using a digital certificate.

```js
test('Sign', () => {
  let signeeName = "Ron Williams";
  let srcDocumentPath = base.myDir + "Document.docx";
  let dstDocumentPath = base.artifactsDir + "SignDocumentCustom.sign.docx";
  let certificatePath = base.myDir + "morzal.pfx";
  let certificatePassword = "aw";

  let signees = createSignees();

  let signeeInfo = signees.find(c => c.name == signeeName);

  if (signeeInfo != null)
    signDocument(srcDocumentPath, dstDocumentPath, signeeInfo, certificatePath, certificatePassword);
  else
    throw new Error("Signee does not exist.");
});


/// <summary>
/// Creates a copy of a source document signed using provided signee information and X509 certificate.
/// </summary>
function signDocument(srcDocumentPath, dstDocumentPath, signeeInfo, certificatePath, certificatePassword) {
  let document = new aw.Document(srcDocumentPath);
  let builder = new aw.DocumentBuilder(document);

  // Configure and insert a signature line, an object in the document that will display a signature that we sign it with.
  let signatureLineOptions = new aw.SignatureLineOptions();
  signatureLineOptions.signer = signeeInfo.name;
  signatureLineOptions.signerTitle = signeeInfo.position;

  let signatureLine = builder.insertSignatureLine(signatureLineOptions).signatureLine;
  signatureLine.id = signeeInfo.personId;

  // First, we will save an unsigned version of our document.
  builder.document.save(dstDocumentPath);

  let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(certificatePath, certificatePassword);

  let signOptions = new aw.DigitalSignatures.SignOptions();
  signOptions.signatureLineId = signeeInfo.personId;
  signOptions.signatureLineImage = signeeInfo.image;

  // Overwrite the unsigned document we saved above with a version signed using the certificate.
  aw.DigitalSignatures.DigitalSignatureUtil.sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
}

function createSignees() {
  let signImagePath = base.imageDir + "Logo.jpg";
  let imageByte = TestUtil.imageToByteArray(signImagePath);
  return [
    {personId: Guid.newGuid().toString(), name: "Ron Williams", position: "Chief Executive Officer", image: imageByte},
    {personId: Guid.newGuid().toString(), name: "Stephen Morse", position: "Head of Compliance", image: imageByte}
  ];
}
```

### See Also

* module [Aspose.Words.DigitalSignatures](../../)
* class [SignOptions](../)

