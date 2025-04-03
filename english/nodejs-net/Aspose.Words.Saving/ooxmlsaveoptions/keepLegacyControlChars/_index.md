---
title: OoxmlSaveOptions.keepLegacyControlChars property
linktitle: keepLegacyControlChars property
articleTitle: keepLegacyControlChars property
second_title: Aspose.Words for NodeJs
description: "OoxmlSaveOptions.keepLegacyControlChars property. Keeps original representation of legacy control characters."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/ooxmlsaveoptions/keepLegacyControlChars/
---

## OoxmlSaveOptions.keepLegacyControlChars property

Keeps original representation of legacy control characters.


```js
get keepLegacyControlChars(): boolean
```

### Examples

Shows how to support legacy control characters when converting to .docx.

```js
let doc = new aw.Document(base.myDir + "Legacy control character.doc");

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "KeepLegacyControlChars" property to "true" to preserve
// the "ShortDateTime" legacy character while saving.
// Set the "KeepLegacyControlChars" property to "false" to remove
// the "ShortDateTime" legacy character from the output document.
let so = new aw.Saving.OoxmlSaveOptions(aw.SaveFormat.Docx);
so.keepLegacyControlChars = keepLegacyControlChars;

doc.save(base.artifactsDir + "OoxmlSaveOptions.keepLegacyControlChars.docx", so);

doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.keepLegacyControlChars.docx");

expect(doc.firstSection.body.getText()).toEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [OoxmlSaveOptions](../)

