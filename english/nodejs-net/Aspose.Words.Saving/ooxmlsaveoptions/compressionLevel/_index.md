---
title: OoxmlSaveOptions.compressionLevel property
linktitle: compressionLevel property
articleTitle: compressionLevel property
second_title: Aspose.Words for Node.js
description: "OoxmlSaveOptions.compressionLevel property. Specifies the compression level used to save document"
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/ooxmlsaveoptions/compressionLevel/
---

## OoxmlSaveOptions.compressionLevel property

Specifies the compression level used to save document.
The default value is [CompressionLevel.Normal](../../compressionlevel/#Normal).



```js
get compressionLevel(): Aspose.Words.Saving.CompressionLevel
```

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

* module [Aspose.Words.Saving](../../)
* class [OoxmlSaveOptions](../)

