---
title: LoadOptions.tempFolder property
linktitle: tempFolder property
articleTitle: tempFolder property
second_title: Aspose.Words for Node.js
description: "LoadOptions.tempFolder property. Allows to use temporary files when reading document"
type: docs
weight: 150
url: /nodejs-net/aspose.words.loading/loadoptions/tempFolder/
---

## LoadOptions.tempFolder property

Allows to use temporary files when reading document.
By default this property is ``null`` and no temporary files are used.



```js
get tempFolder(): string
```

### Remarks

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.




### Examples

Shows how to use the hard drive instead of memory when loading a document.

```js
// When we load a document, various elements are temporarily stored in memory as the save operation occurs.
// We can use this option to use a temporary folder in the local file system instead,
// which will reduce our application's memory overhead.
let options = new aw.Loading.LoadOptions();
options.tempFolder = base.artifactsDir + "TempFiles";

// The specified temporary folder must exist in the local file system before the load operation.
if (!fs.existsSync(options.tempFolder)) {
  fs.mkdirSync(options.tempFolder);
}

let doc = new aw.Document(base.myDir + "Document.docx", options);

// The folder will persist with no residual contents from the load operation.
expect(fs.readdirSync(options.tempFolder).length).toEqual(0);
```

Shows how to load a document using temporary files.

```js
// Note that such an approach can reduce memory usage but degrades speed
const loadOptions = new aw.Loading.LoadOptions();
loadOptions.tempFolder = "C:\\Temp\\";

// Ensure that the directory exists and load
if (!fs.existsSync(loadOptions.tempFolder)){
  fs.mkdirSync(loadOptions.tempFolder);
}    

const doc = new aw.Document(base.myDir + "Document.docx", loadOptions);
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

