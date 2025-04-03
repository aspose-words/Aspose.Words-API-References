---
title: FileFormatInfo.hasDigitalSignature property
linktitle: hasDigitalSignature property
articleTitle: hasDigitalSignature property
second_title: Aspose.Words for NodeJs
description: "FileFormatInfo.hasDigitalSignature property. Returns ``true`` if this document contains a digital signature"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words/fileformatinfo/hasDigitalSignature/
---

## FileFormatInfo.hasDigitalSignature property

Returns ``true`` if this document contains a digital signature.
This property merely informs that a digital signature is present on a document,
but it does not  specify whether the signature is valid or not.



```js
get hasDigitalSignature(): boolean
```

### Remarks

This property exists to help you sort documents that are digitally signed from those that are not.
If you use Aspose.Words to modify and save a document that is digitally signed, then the digital signature will
be lost. This is by design because a digital signature exists to guard the authenticity of a document.
Using this property you can detect digitally signed documents before processing them in the same way as normal
documents and take some action to avoid losing the digital signature, for example notify the user.




### Examples

Shows how to add a digital signature to a document.

```js
string signedFile = base.myDir + "File.DetectDigitalSignatures.docx";
if (fs.existsSync(signedFile))
  File.delete(signedFile);

let info = aw.FileFormatUtil.detectFileFormat(base.myDir + "Document.docx");

expect(aw.FileFormatUtil.loadFormatToExtension(info.loadFormat)).toEqual(".docx");
expect(info.hasDigitalSignature).toEqual(false);

let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw", null);
aw.DigitalSignatures.DigitalSignatureUtil.sign(base.myDir + "Document.docx", signedFile,
  certificateHolder, new aw.DigitalSignatures.SignOptions() { SignTime = Date.now() });
```

Shows how to use the FileFormatUtil class to detect the document format and presence of digital signatures.

```js
// Use a FileFormatInfo instance to verify that a document is not digitally signed.
let info = aw.FileFormatUtil.detectFileFormat(base.myDir + "Document.docx");

expect(aw.FileFormatUtil.loadFormatToExtension(info.loadFormat)).toEqual(".docx");
expect(info.hasDigitalSignature).toEqual(false);

let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw", null);
let signOptions = new aw.DigitalSignatures.SignOptions();
signOptions.signTime = Date.now();
aw.DigitalSignatures.DigitalSignatureUtil.sign(base.myDir + "Document.docx", base.artifactsDir + "File.DetectDigitalSignatures.docx",
  certificateHolder, signOptions);

// Use a new FileFormatInstance to confirm that it is signed.
info = aw.FileFormatUtil.detectFileFormat(base.artifactsDir + "File.DetectDigitalSignatures.docx");

expect(info.hasDigitalSignature).toEqual(true);

// We can load and access the signatures of a signed document in a collection like this.
expect(aw.DigitalSignatures.DigitalSignatureUtil.loadSignatures(base.artifactsDir + "File.DetectDigitalSignatures.docx").count).toEqual(1);
```

### See Also

* module [Aspose.Words](../../)
* class [FileFormatInfo](../)

