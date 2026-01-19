---
title: CertificateHolder class
linktitle: CertificateHolder class
articleTitle: CertificateHolder class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DigitalSignatures.CertificateHolder class. Represents a holder of X509Certificate2 instance"
type: docs
weight: 10
url: /nodejs-net/aspose.words.digitalsignatures/certificateholder/
---

## CertificateHolder class

Represents a holder of **X509Certificate2** instance.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/nodejs-net/working-with-digital-signatures/) documentation article.




### Remarks

[CertificateHolder](./) can be created by static factory methods only. 
It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system.
This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with 
 as parameters.




### Methods

| Name | Description |
| --- | --- |
|[ create(certBytes, password)](./create/#number[]_unknown) | Creates [CertificateHolder](./) object using byte array of PKCS12 store and its password. |
|[ create(certBytes, password)](./create/#number[]_string) | Creates [CertificateHolder](./) object using byte array of PKCS12 store and its password. |
|[ create(fileName, password)](./create/#string_string) | Creates [CertificateHolder](./) object using path to PKCS12 store and its password. |
|[ create(fileName, password, alias)](./create/#string_string_string) | Creates [CertificateHolder](./) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found. |

### Examples

Shows how to digitally sign documents.

```js
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");

// Create a comment and date which will be applied with our new digital signature.
let signOptions = new aw.DigitalSignatures.SignOptions
{
  Comments = "My comment",
  SignTime = Date.now()
};

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
using (Stream streamIn = new FileStream(base.myDir + "Document.docx", FileMode.open))
{
  using (Stream streamOut = new FileStream(base.artifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
  {
    aw.DigitalSignatures.DigitalSignatureUtil.sign(streamIn, streamOut, certificateHolder, signOptions);
  }
}
```

Shows how to sign encrypted document file.

```js
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");

// Create a comment, date, and decryption password which will be applied with our new digital signature.
let signOptions = new aw.DigitalSignatures.SignOptions
{
  Comments = "Comment",
  SignTime = Date.now(),
  DecryptionPassword = "docPassword"
};

// Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
string inputFileName = base.myDir + "Encrypted.docx";
string outputFileName = base.artifactsDir + "DigitalSignatureUtil.decryptionPassword.docx";

aw.DigitalSignatures.DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

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

* module [Aspose.Words.DigitalSignatures](../)

