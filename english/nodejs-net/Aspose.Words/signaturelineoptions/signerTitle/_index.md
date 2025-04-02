---
title: SignatureLineOptions.signerTitle property
linktitle: signerTitle property
articleTitle: signerTitle property
second_title: Aspose.Words for NodeJs
description: "SignatureLineOptions.signerTitle property. Gets or sets suggested signer's title"
type: docs
weight: 80
url: /nodejs-net/Aspose.Words/signaturelineoptions/signerTitle/
---

## SignatureLineOptions.signerTitle property

Gets or sets suggested signer's title.
Default value for this property is **empty string** ().



```js
get signerTitle(): string
```

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

* module [Aspose.Words](../../)
* class [SignatureLineOptions](../)

