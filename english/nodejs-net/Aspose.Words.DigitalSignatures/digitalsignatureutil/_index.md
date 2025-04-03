---
title: DigitalSignatureUtil class
linktitle: DigitalSignatureUtil class
articleTitle: DigitalSignatureUtil class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DigitalSignatures.DigitalSignatureUtil class. Provides methods for signing document"
type: docs
weight: 40
url: /nodejs-net/aspose.words.digitalsignatures/digitalsignatureutil/
---

## DigitalSignatureUtil class

Provides methods for signing document.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/nodejs-net/working-with-digital-signatures/) documentation article.




### Remarks

Since digital signature works with file content rather than Document Object Model these methods are put into a separate class.

Supported formats are:
[LoadFormat.Doc](../../aspose.words/loadformat/#Doc),
[LoadFormat.Dot](../../aspose.words/loadformat/#Dot),
[LoadFormat.Docx](../../aspose.words/loadformat/#Docx),
[LoadFormat.Dotx](../../aspose.words/loadformat/#Dotx),
[LoadFormat.Docm](../../aspose.words/loadformat/#Docm),
[LoadFormat.Odt](../../aspose.words/loadformat/#Odt),
[LoadFormat.Ott](../../aspose.words/loadformat/#Ott).




### Methods

| Name | Description |
| --- | --- |
|[ loadSignatures(fileName)](./loadSignatures/#string) | Loads digital signatures from document. |
|[ loadSignatures(stream)](./loadSignatures/#buffer) | Loads digital signatures from document using stream. |
|[ removeAllSignatures(srcStream, dstStream)](./removeAllSignatures/#buffer_unknown) |  |
|[ removeAllSignatures(srcFileName, dstFileName)](./removeAllSignatures/#string_string) | Removes all digital signatures from source file and writes unsigned file to destination file. The following formats are compatible for digital signature removal: [LoadFormat.Doc](../../aspose.words/loadformat/#Doc), [LoadFormat.Dot](../../aspose.words/loadformat/#Dot), [LoadFormat.Docx](../../aspose.words/loadformat/#Docx), [LoadFormat.Dotx](../../aspose.words/loadformat/#Dotx), [LoadFormat.Docm](../../aspose.words/loadformat/#Docm), [LoadFormat.Odt](../../aspose.words/loadformat/#Odt), [LoadFormat.Ott](../../aspose.words/loadformat/#Ott). |
|[ sign(srcStream, dstStream, certHolder, signOptions)](./sign/#buffer_buffer_certificateholder_signoptions) | Signs source document using given [CertificateHolder](../certificateholder/) and [SignOptions](../signoptions/) with digital signature and writes signed document to destination stream. Supported formats are: [LoadFormat.Doc](../../aspose.words/loadformat/#Doc), [LoadFormat.Dot](../../aspose.words/loadformat/#Dot), [LoadFormat.Docx](../../aspose.words/loadformat/#Docx), [LoadFormat.Dotx](../../aspose.words/loadformat/#Dotx), [LoadFormat.Docm](../../aspose.words/loadformat/#Docm), [LoadFormat.Odt](../../aspose.words/loadformat/#Odt), [LoadFormat.Ott](../../aspose.words/loadformat/#Ott). |
|[ sign(srcFileName, dstFileName, certHolder, signOptions)](./sign/#string_string_certificateholder_signoptions) | Signs source document using given [CertificateHolder](../certificateholder/) and [SignOptions](../signoptions/) with digital signature and writes signed document to destination file. Supported formats are: [LoadFormat.Doc](../../aspose.words/loadformat/#Doc), [LoadFormat.Dot](../../aspose.words/loadformat/#Dot), [LoadFormat.Docx](../../aspose.words/loadformat/#Docx), [LoadFormat.Dotx](../../aspose.words/loadformat/#Dotx), [LoadFormat.Docm](../../aspose.words/loadformat/#Docm), [LoadFormat.Odt](../../aspose.words/loadformat/#Odt), [LoadFormat.Ott](../../aspose.words/loadformat/#Ott). |
|[ sign(srcStream, dstStream, certHolder)](./sign/#buffer_buffer_certificateholder) | Signs source document using given [CertificateHolder](../certificateholder/) with digital signature and writes signed document to destination stream. Supported formats are: [LoadFormat.Doc](../../aspose.words/loadformat/#Doc), [LoadFormat.Dot](../../aspose.words/loadformat/#Dot), [LoadFormat.Docx](../../aspose.words/loadformat/#Docx), [LoadFormat.Dotx](../../aspose.words/loadformat/#Dotx), [LoadFormat.Docm](../../aspose.words/loadformat/#Docm), [LoadFormat.Odt](../../aspose.words/loadformat/#Odt), [LoadFormat.Ott](../../aspose.words/loadformat/#Ott). |
|[ sign(srcFileName, dstFileName, certHolder)](./sign/#string_string_certificateholder) | Signs source document using given [CertificateHolder](../certificateholder/) with digital signature and writes signed document to destination file. Supported formats are: [LoadFormat.Doc](../../aspose.words/loadformat/#Doc), [LoadFormat.Dot](../../aspose.words/loadformat/#Dot), [LoadFormat.Docx](../../aspose.words/loadformat/#Docx), [LoadFormat.Dotx](../../aspose.words/loadformat/#Dotx), [LoadFormat.Docm](../../aspose.words/loadformat/#Docm), [LoadFormat.Odt](../../aspose.words/loadformat/#Odt), [LoadFormat.Ott](../../aspose.words/loadformat/#Ott). |

### Examples

Shows how to load signatures from a digitally signed document.

```js
// There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
// 1 -  Load from a document from a local file system filename:
let digitalSignatures =
  aw.DigitalSignatures.DigitalSignatureUtil.loadSignatures(base.myDir + "Digitally signed.docx");

// If this collection is nonempty, then we can verify that the document is digitally signed.
expect(digitalSignatures.count).toEqual(1);

// 2 -  Load from a document from a Buffer:
let data = base.loadFileToBuffer(base.myDir + "Digitally signed.docx");
digitalSignatures = aw.DigitalSignatures.DigitalSignatureUtil.loadSignatures(data);
expect(digitalSignatures.count).toEqual(1);
```

Shows how to remove digital signatures from a digitally signed document.

```js
// There are two ways of using the DigitalSignatureUtil class to remove digital signatures
// from a signed document by saving an unsigned copy of it somewhere else in the local file system.
// 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
aw.DigitalSignatures.DigitalSignatureUtil.removeAllSignatures(base.myDir + "Digitally signed.docx",
  base.artifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
let streamIn = base.loadFileToBuffer(base.myDir + "Digitally signed.docx");
let streamOut = fs.createWriteStream(base.artifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx");

aw.DigitalSignatures.DigitalSignatureUtil.removeAllSignatures(streamIn, streamOut);
await new Promise(resolve => streamOut.on("finish", resolve));

// Verify that both our output documents have no digital signatures.
expect(aw.DigitalSignatures.DigitalSignatureUtil.loadSignatures(base.artifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").count).toEqual(0);
expect(aw.DigitalSignatures.DigitalSignatureUtil.loadSignatures(base.artifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").count).toEqual(0);
```

### See Also

* module [Aspose.Words.DigitalSignatures](../)

