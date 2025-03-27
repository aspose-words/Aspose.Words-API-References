---
title: DocSaveOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for NodeJs
description: "DocSaveOptions.password property. Gets/sets a password to encrypt document using RC4 encryption method."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/docsaveoptions/password/
---

## DocSaveOptions.password property

Gets/sets a password to encrypt document using RC4 encryption method.


```js
get password(): string
```

### Remarks

In order to save document without encryption this property should be ``None`` or empty string.




### Examples

Shows how to set save options for older Microsoft Word formats.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.write("Hello world!");

let options = new aw.Saving.DocSaveOptions(aw.SaveFormat.Doc);

// Set a password which will protect the loading of the document by Microsoft Word or Aspose.words.
// Note that this does not encrypt the contents of the document in any way.
options.password = "MyPassword";

// If the document contains a routing slip, we can preserve it while saving by setting this flag to true.
options.saveRoutingSlip = true;

doc.save(base.artifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// To be able to load the document,
// we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
expect(() => doc = new aw.Document(base.artifactsDir + "DocSaveOptions.SaveAsDoc.doc")).toThrow("The document password is incorrect.");

let loadOptions = new aw.Loading.LoadOptions("MyPassword");
doc = new aw.Document(base.artifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

expect(doc.getText().trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [DocSaveOptions](../)

