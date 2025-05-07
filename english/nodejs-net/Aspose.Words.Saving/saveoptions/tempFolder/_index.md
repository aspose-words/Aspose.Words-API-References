---
title: SaveOptions.tempFolder property
linktitle: tempFolder property
articleTitle: tempFolder property
second_title: Aspose.Words for Node.js
description: "SaveOptions.tempFolder property. Specifies the folder for temporary files used when saving to a DOC or DOCX file"
type: docs
weight: 110
url: /nodejs-net/aspose.words.saving/saveoptions/tempFolder/
---

## SaveOptions.tempFolder property

Specifies the folder for temporary files used when saving to a DOC or DOCX file.
By default this property is ``null`` and no temporary files are used.



```js
get tempFolder(): string
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(OutOfMemoryException)) | Throw if you are saving a very large document (thousands of pages) and/or processing many documents at the same time. The memory spike during saving can be significant enough to cause the exception. |

### Remarks

When Aspose.Words saves a document, it needs to create temporary internal structures. By default,
these internal structures are created in memory and the memory usage spikes for a short period while
the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

Specifying a temporary folder using [SaveOptions.tempFolder](./) will cause Aspose.Words to keep the internal structures in
temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.




### Examples

Shows how to use the hard drive instead of memory when saving a document.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// When we save a document, various elements are temporarily stored in memory as the save operation is taking place.
// We can use this option to use a temporary folder in the local file system instead,
// which will reduce our application's memory overhead.
let options = new aw.Saving.DocSaveOptions();
options.tempFolder = base.artifactsDir + "TempFiles";

// The specified temporary folder must exist in the local file system before the save operation.
if (!fs.existsSync(options.tempFolder))
  fs.mkdirSync(options.tempFolder);

doc.save(base.artifactsDir + "DocSaveOptions.tempFolder.doc", options);

// The folder will persist with no residual contents from the load operation.
const fileList = fs.readdirSync(options.tempFolder);    
expect(fileList.length).toEqual(0);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

