---
title: DigitalSignatureUtil.removeAllSignatures method
linktitle: removeAllSignatures method
articleTitle: removeAllSignatures method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DigitalSignatures.DigitalSignatureUtil.removeAllSignatures method"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.DigitalSignatures/digitalsignatureutil/removeAllSignatures/
---

## removeAllSignatures(srcStream, dstStream) {#buffer_unknown}

```js
removeAllSignatures(srcStream: BufferdstStream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | Buffer |  |
| dstStream |  |  |

## removeAllSignatures(srcFileName, dstFileName) {#string_string}

Removes all digital signatures from source file and writes unsigned file to destination file.
The following formats are compatible for digital signature removal:
[LoadFormat.Doc](../../../aspose.words/loadformat/#Doc),
[LoadFormat.Dot](../../../aspose.words/loadformat/#Dot),
[LoadFormat.Docx](../../../aspose.words/loadformat/#Docx),
[LoadFormat.Dotx](../../../aspose.words/loadformat/#Dotx),
[LoadFormat.Docm](../../../aspose.words/loadformat/#Docm),
[LoadFormat.Odt](../../../aspose.words/loadformat/#Odt),
[LoadFormat.Ott](../../../aspose.words/loadformat/#Ott).




```js
removeAllSignatures(srcFileName: stringdstFileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | string |  |
| dstFileName | string |  |

## Examples

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

