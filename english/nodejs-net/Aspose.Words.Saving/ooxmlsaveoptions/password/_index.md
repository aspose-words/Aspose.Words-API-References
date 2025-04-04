---
title: OoxmlSaveOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Node.js
description: "OoxmlSaveOptions.password property. Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm."
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/ooxmlsaveoptions/password/
---

## OoxmlSaveOptions.password property

Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm.


```js
get password(): string
```

### Remarks

In order to save document without encryption this property should be ``null`` or empty string.




### Examples

Shows how to create a password encrypted Office Open XML document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

let saveOptions = new aw.Saving.OoxmlSaveOptions();
saveOptions.password = "MyPassword";

doc.save(base.artifactsDir + "OoxmlSaveOptions.password.docx", saveOptions);

// We will not be able to open this document with Microsoft Word or
// Aspose.words without providing the correct password.
//Assert.Throws<IncorrectPasswordException>(() => doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.password.docx"));
expect(() => { doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.password.docx"); }).toThrow();

// Open the encrypted document by passing the correct password in a LoadOptions object.
doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.password.docx", new aw.Loading.LoadOptions("MyPassword"));

expect(doc.getText().trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [OoxmlSaveOptions](../)

