---
title: ImportFormatOptions.forceCopyStyles property
linktitle: forceCopyStyles property
articleTitle: forceCopyStyles property
second_title: Aspose.Words for NodeJs
description: "ImportFormatOptions.forceCopyStyles property. Gets or sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KeepSourceFormatting](../../importformatmode/#KeepSourceFormatting) mode"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words/importformatoptions/forceCopyStyles/
---

## ImportFormatOptions.forceCopyStyles property

Gets or sets a boolean value indicating either to copy conflicting styles
in [ImportFormatMode.KeepSourceFormatting](../../importformatmode/#KeepSourceFormatting) mode.
The default value is ``false``.



```js
get forceCopyStyles(): boolean
```

### Remarks

By default, if a matching style already exists in a destination document, the source style formatting
is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to ``true``, the source style will be forcibly copied
into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document
will be preserved.




### Examples

Shows how to copy source styles with unique names forcibly.

```js
// Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
const srcDoc = new aw.Document(base.myDir + "Styles source.docx");
const dstDoc = new aw.Document(base.myDir + "Styles destination.docx");

const options = new aw.ImportFormatOptions();
options.forceCopyStyles = true;
dstDoc.appendDocument(srcDoc, aw.ImportFormatMode.KeepSourceFormatting, options);

const paras = dstDoc.sections.at(1).body.paragraphs;

expect(paras.at(0).paragraphFormat.style.name).toEqual("MyStyle1_0");
expect(paras.at(1).paragraphFormat.style.name).toEqual("MyStyle2_0");
expect(paras.at(2).paragraphFormat.style.name).toEqual("MyStyle3");
```

### See Also

* module [Aspose.Words](../../)
* class [ImportFormatOptions](../)

