---
title: DigitalSignatureUtil.loadSignatures method
linktitle: loadSignatures method
articleTitle: loadSignatures method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DigitalSignatures.DigitalSignatureUtil.loadSignatures method"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.DigitalSignatures/digitalsignatureutil/loadSignatures/
---

## loadSignatures(fileName) {#string}

Loads digital signatures from document.


```js
loadSignatures(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | Path to the document. |

### Returns

Collection of digital signatures. Returns empty collection if file is not signed.


## loadSignatures(stream) {#buffer}

Loads digital signatures from document using stream.


```js
loadSignatures(stream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | Stream with the document. |

### Returns

Collection of digital signatures. Returns empty collection if file is not signed.


## Examples

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

## See Also

* module [Aspose.Words.DigitalSignatures](../../)
* class [DigitalSignatureUtil](../)

