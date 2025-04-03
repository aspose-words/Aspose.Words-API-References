---
title: DigitalSignatureUtil.sign method
linktitle: sign method
articleTitle: sign method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DigitalSignatures.DigitalSignatureUtil.sign method"
type: docs
weight: 30
url: /nodejs-net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---

## sign(srcStream, dstStream, certHolder, signOptions) {#buffer_buffer_certificateholder_signoptions}

Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/)
with digital signature and writes signed document to destination stream.
Supported formats are:
[LoadFormat.Doc](../../../aspose.words/loadformat/#Doc),
[LoadFormat.Dot](../../../aspose.words/loadformat/#Dot),
[LoadFormat.Docx](../../../aspose.words/loadformat/#Docx),
[LoadFormat.Dotx](../../../aspose.words/loadformat/#Dotx),
[LoadFormat.Docm](../../../aspose.words/loadformat/#Docm),
[LoadFormat.Odt](../../../aspose.words/loadformat/#Odt),
[LoadFormat.Ott](../../../aspose.words/loadformat/#Ott).

**Output will be written to the start of stream and stream size will be updated with content length.**





```js
sign(srcStream: BufferdstStream: BuffercertHolder: Aspose.Words.DigitalSignatures.CertificateHoldersignOptions: Aspose.Words.DigitalSignatures.SignOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | Buffer | The stream which contains the document to sign. |
| dstStream | Buffer | The stream that signed document will be written to. |
| certHolder | [CertificateHolder](../../certificateholder/) | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |
| signOptions | [SignOptions](../../signoptions/) | [SignOptions](../../signoptions/) object with various signing options. |

## sign(srcFileName, dstFileName, certHolder, signOptions) {#string_string_certificateholder_signoptions}

Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/)
with digital signature and writes signed document to destination file.
Supported formats are:
[LoadFormat.Doc](../../../aspose.words/loadformat/#Doc),
[LoadFormat.Dot](../../../aspose.words/loadformat/#Dot),
[LoadFormat.Docx](../../../aspose.words/loadformat/#Docx),
[LoadFormat.Dotx](../../../aspose.words/loadformat/#Dotx),
[LoadFormat.Docm](../../../aspose.words/loadformat/#Docm),
[LoadFormat.Odt](../../../aspose.words/loadformat/#Odt),
[LoadFormat.Ott](../../../aspose.words/loadformat/#Ott).




```js
sign(srcFileName: stringdstFileName: stringcertHolder: Aspose.Words.DigitalSignatures.CertificateHoldersignOptions: Aspose.Words.DigitalSignatures.SignOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | string | The file name of the document to sign. |
| dstFileName | string | The file name of the signed document output. |
| certHolder | [CertificateHolder](../../certificateholder/) | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |
| signOptions | [SignOptions](../../signoptions/) | [SignOptions](../../signoptions/) object with various signing options. |

## sign(srcStream, dstStream, certHolder) {#buffer_buffer_certificateholder}

Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature
and writes signed document to destination stream.
Supported formats are:
[LoadFormat.Doc](../../../aspose.words/loadformat/#Doc),
[LoadFormat.Dot](../../../aspose.words/loadformat/#Dot),
[LoadFormat.Docx](../../../aspose.words/loadformat/#Docx),
[LoadFormat.Dotx](../../../aspose.words/loadformat/#Dotx),
[LoadFormat.Docm](../../../aspose.words/loadformat/#Docm),
[LoadFormat.Odt](../../../aspose.words/loadformat/#Odt),
[LoadFormat.Ott](../../../aspose.words/loadformat/#Ott).

**Output will be written to the start of stream and stream size will be updated with content length.**





```js
sign(srcStream: BufferdstStream: BuffercertHolder: Aspose.Words.DigitalSignatures.CertificateHolder)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | Buffer | The stream which contains the document to sign. |
| dstStream | Buffer | The stream that signed document will be written to. |
| certHolder | [CertificateHolder](../../certificateholder/) | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |

## sign(srcFileName, dstFileName, certHolder) {#string_string_certificateholder}

Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature
and writes signed document to destination file.
Supported formats are:
[LoadFormat.Doc](../../../aspose.words/loadformat/#Doc),
[LoadFormat.Dot](../../../aspose.words/loadformat/#Dot),
[LoadFormat.Docx](../../../aspose.words/loadformat/#Docx),
[LoadFormat.Dotx](../../../aspose.words/loadformat/#Dotx),
[LoadFormat.Docm](../../../aspose.words/loadformat/#Docm),
[LoadFormat.Odt](../../../aspose.words/loadformat/#Odt),
[LoadFormat.Ott](../../../aspose.words/loadformat/#Ott).




```js
sign(srcFileName: stringdstFileName: stringcertHolder: Aspose.Words.DigitalSignatures.CertificateHolder)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | string | The file name of the document to sign. |
| dstFileName | string | The file name of the signed document output. |
| certHolder | [CertificateHolder](../../certificateholder/) | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |

## Examples

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

## See Also

* module [Aspose.Words.DigitalSignatures](../../)
* class [DigitalSignatureUtil](../)

