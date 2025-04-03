---
title: SaveOptions.createSaveOptions method
linktitle: createSaveOptions method
articleTitle: createSaveOptions method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.SaveOptions.createSaveOptions method"
type: docs
weight: 200
url: /nodejs-net/aspose.words.saving/saveoptions/createSaveOptions/
---

## createSaveOptions(saveFormat) {#saveformat}

Creates a save options object of a class suitable for the specified save format.


```js
createSaveOptions(saveFormat: Aspose.Words.SaveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | [SaveFormat](../../../aspose.words/saveformat/) | The save format for which to create a save options object. |

### Returns

An object of a class that derives from [SaveOptions](../).


## createSaveOptions(fileName) {#string}

Creates a save options object of a class suitable for the file extension specified in the given file name.


```js
createSaveOptions(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The extension of this file name determines the class of the save options object to create. |

### Returns

An object of a class that derives from [SaveOptions](../).


## Examples

Shows an option to optimize memory consumption when rendering large documents to PDF.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = aw.Saving.SaveOptions.createSaveOptions(aw.SaveFormat.Pdf);

// Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
// at the cost of increasing the duration of the operation.
// Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
saveOptions.memoryOptimization = memoryOptimization;

doc.save(base.artifactsDir + "PdfSaveOptions.memoryOptimization.pdf", saveOptions);
```

## See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

