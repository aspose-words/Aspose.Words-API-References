---
title: ImportFormatOptions.keepSourceNumbering property
linktitle: keepSourceNumbering property
articleTitle: keepSourceNumbering property
second_title: Aspose.Words for NodeJs
description: "ImportFormatOptions.keepSourceNumbering property. Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words/importformatoptions/keepSourceNumbering/
---

## ImportFormatOptions.keepSourceNumbering property

Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and
destination documents.
The default value is ``False``.



```js
get keepSourceNumbering(): boolean
```

### Examples

Shows how to import a document with numbered lists.

```js
const srcDoc = new aw.Document(base.myDir + "List source.docx");
const dstDoc = new aw.Document(base.myDir + "List destination.docx");

expect(dstDoc.lists.count).toEqual(4);

const options = new aw.ImportFormatOptions();

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
options.keepSourceNumbering = isKeepSourceNumbering;

dstDoc.appendDocument(srcDoc, aw.ImportFormatMode.KeepSourceFormatting, options);
dstDoc.updateListLabels();

expect(dstDoc.lists.count).toEqual(isKeepSourceNumbering ? 5 : 4);
```

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

```js
const srcDoc = new aw.Document(base.myDir + "List with the same definition identifier - source.docx");
const dstDoc = new aw.Document(base.myDir + "List with the same definition identifier - destination.docx");

// Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
// to identical styles as Aspose.Words imports them into destination documents.
const importFormatOptions = new aw.ImportFormatOptions();
importFormatOptions.keepSourceNumbering = true;

dstDoc.appendDocument(srcDoc, aw.ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.updateListLabels();
```

Shows how to resolve list numbering clashes in source and destination documents.

```js
// Open a document with a custom list numbering scheme, and then clone it.
// Since both have the same numbering format, the formats will clash if we import one document into the other.
let srcDoc = new aw.Document(base.myDir + "Custom list numbering.docx");
let dstDoc = srcDoc.clone();

// When we import the document's clone into the original and then append it,
// then the two lists with the same list format will join.
// If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
// that we append to the original will carry on the numbering of the list we append it to.
// This will effectively merge the two lists into one.
// If we set the "KeepSourceNumbering" flag to "true", then the document clone
// list will preserve its original numbering, making the two lists appear as separate lists. 
let importFormatOptions = new aw.ImportFormatOptions();
importFormatOptions.keepSourceNumbering = keepSourceNumbering;

let importer = new aw.NodeImporter(srcDoc, dstDoc, aw.ImportFormatMode.KeepDifferentStyles, importFormatOptions);
for (let paragraph of srcDoc.firstSection.body.paragraphs)
{
  let importedNode = importer.importNode(paragraph, true);
  dstDoc.firstSection.body.appendChild(importedNode);
}

dstDoc.updateListLabels();

if (keepSourceNumbering)
{
  expect(dstDoc.firstSection.body.toString(aw.SaveFormat.Text).trim()).toEqual(
    "6. Item 1\r\n" +
    "7. Item 2 \r\n" +
    "8. Item 3\r\n" +
    "9. Item 4\r\n" +
    "6. Item 1\r\n" +
    "7. Item 2 \r\n" +
    "8. Item 3\r\n" +
    "9. Item 4");
}
else
{
  expect(dstDoc.firstSection.body.toString(aw.SaveFormat.Text).trim()).toEqual(
    "6. Item 1\r\n" +
    "7. Item 2 \r\n" +
    "8. Item 3\r\n" +
    "9. Item 4\r\n" +
    "10. Item 1\r\n" +
    "11. Item 2 \r\n" +
    "12. Item 3\r\n" +
    "13. Item 4");
}
```

### See Also

* module [Aspose.Words](../../)
* class [ImportFormatOptions](../)

