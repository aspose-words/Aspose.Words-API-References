---
title: FileFormatInfo class
linktitle: FileFormatInfo class
articleTitle: FileFormatInfo class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.FileFormatInfo class. Contains data returned by [FileFormatUtil](../fileformatutil/) document format detection methods"
type: docs
weight: 430
url: /nodejs-net/aspose.words/fileformatinfo/
---

## FileFormatInfo class

Contains data returned by [FileFormatUtil](../fileformatutil/) document format detection methods.
To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/nodejs-net/detect-file-format-and-check-format-compatibility/) documentation article.




### Remarks

You do not create instances of this class directly. Objects of this class are returned by
[FileFormatUtil.detectFileFormat()](../fileformatutil/detectFileFormat/#buffer) methods.




### Properties

| Name | Description |
| --- | --- |
| [encoding](./encoding/) | Gets the detected encoding if applicable to the current document format. At the moment detects encoding only for HTML documents. |
| [hasDigitalSignature](./hasDigitalSignature/) | Returns ``true`` if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not  specify whether the signature is valid or not. |
| [hasMacros](./hasMacros/) | Returns ``true`` if this document contains a VBA macros. |
| [isEncrypted](./isEncrypted/) | Returns ``true`` if the document is encrypted and requires a password to open. |
| [loadFormat](./loadFormat/) | Gets the detected document format. |

### Examples

Shows how to use the FileFormatUtil class to detect the document format and encryption.

```js
let doc = new aw.Document();

// Configure a SaveOptions object to encrypt the document
// with a password when we save it, and then save the document.
let saveOptions = new aw.Saving.OdtSaveOptions(aw.SaveFormat.Odt);
saveOptions.password = "MyPassword";

doc.save(base.artifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verify the file type of our document, and its encryption status.
let info = aw.FileFormatUtil.detectFileFormat(base.artifactsDir + "File.DetectDocumentEncryption.odt");

expect(aw.FileFormatUtil.loadFormatToExtension(info.loadFormat)).toEqual(".odt");
expect(info.isEncrypted).toEqual(true);
```

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

* module [Aspose.Words](../)

