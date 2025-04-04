---
title: CompressionLevel enumeration
linktitle: CompressionLevel enumeration
articleTitle: CompressionLevel enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.CompressionLevel enumeration. Compression level for OOXML files"
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/compressionlevel/
---

## CompressionLevel enumeration

Compression level for OOXML files. 
(DOCX and DOTX files are internally a ZIP-archive, this property controls the compression level of the archive.

Note, that FlatOpc file is not a ZIP-archive, therefore, this property does not affect the FlatOpc files.)




### Members

| Name | Description |
| --- | --- |
| Normal | Normal compression level. Default compression level used by Aspose.Words. |
| Maximum | Maximum compression level. |
| Fast | Fast compression level. |
| SuperFast | Super Fast compression level. Microsoft Word uses this compression level. |

### Examples

Shows how to specify the compression level to use while saving an OOXML document.

```js
let doc = new aw.Document(base.myDir + "Big document.docx");

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "CompressionLevel" property to "CompressionLevel.Maximum" to apply the strongest and slowest compression.
// Set the "CompressionLevel" property to "CompressionLevel.Normal" to apply
// the default compression that Aspose.words uses while saving OOXML documents.
// Set the "CompressionLevel" property to "CompressionLevel.Fast" to apply a faster and weaker compression.
// Set the "CompressionLevel" property to "CompressionLevel.SuperFast" to apply
// the default compression that Microsoft Word uses.
let saveOptions = new aw.Saving.OoxmlSaveOptions(aw.SaveFormat.Docx);
saveOptions.compressionLevel = compressionLevel;

let timeBefore = new Date();
doc.save(base.artifactsDir + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
let timeAfter = new Date();

let testedFileLength = fs.statSync(base.artifactsDir + "OoxmlSaveOptions.DocumentCompression.docx").size;

console.log(`Saving operation done using the \"${compressionLevel}\" compression level:`);
console.log(`\tDuration:\t${timeAfter - timeBefore} ms`);
console.log(`\tFile Size:\t${testedFileLength} bytes`);
```

### See Also

* module [Aspose.Words.Saving](../)

