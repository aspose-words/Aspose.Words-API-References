---
title: FileFormatInfo.loadFormat property
linktitle: loadFormat property
articleTitle: loadFormat property
second_title: Aspose.Words for NodeJs
description: "FileFormatInfo.loadFormat property. Gets the detected document format."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/fileformatinfo/loadFormat/
---

## FileFormatInfo.loadFormat property

Gets the detected document format.


```js
get loadFormat(): Aspose.Words.LoadFormat
```

### Remarks

When an OOXML document is encrypted, it is not possible to ascertain whether it is
an Excel, Word or PowerPoint document without decrypting it first so for an encrypted OOXML
document this property will always return [LoadFormat.Docx](../../loadformat/#Docx).




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

Shows how to use the FileFormatUtil methods to detect the format of a document.

```js
// Load a document from a file that is missing a file extension, and then detect its file format.
let docStream = base.loadFileToBuffer(base.myDir + "Word document with missing file extension");
let info = aw.FileFormatUtil.detectFileFormat(docStream);
let loadFormat = info.loadFormat;
expect(loadFormat).toEqual(aw.LoadFormat.Doc);
// Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
// 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
let fileExtension = aw.FileFormatUtil.loadFormatToExtension(loadFormat);
let saveFormat = aw.FileFormatUtil.extensionToSaveFormat(fileExtension);
// 2 -  Convert the LoadFormat directly to its SaveFormat:
saveFormat = aw.FileFormatUtil.loadFormatToSaveFormat(loadFormat);
// Load a document from the stream, and then save it to the automatically detected file extension.
let doc = new aw.Document(docStream);
expect(aw.FileFormatUtil.saveFormatToExtension(saveFormat)).toEqual(".doc");
doc.save(base.artifactsDir + "File.SaveToDetectedFileFormat" + aw.FileFormatUtil.saveFormatToExtension(saveFormat));
```

### See Also

* module [Aspose.Words](../../)
* class [FileFormatInfo](../)
* property [FileFormatInfo.isEncrypted](../isEncrypted/)

