---
title: Document.appendDocument method
linktitle: appendDocument method
articleTitle: appendDocument method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Document.appendDocument method"
type: docs
weight: 550
url: /nodejs-net/aspose.words/document/appendDocument/
---

## appendDocument(srcDoc, importFormatMode) {#document_importformatmode}

Appends the specified document to the end of this document.


```js
appendDocument(srcDoc: Aspose.Words.DocumentimportFormatMode: Aspose.Words.ImportFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../) | The document to append. |
| importFormatMode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |

## appendDocument(srcDoc, importFormatMode, importFormatOptions) {#document_importformatmode_importformatoptions}

Appends the specified document to the end of this document.


```js
appendDocument(srcDoc: Aspose.Words.DocumentimportFormatMode: Aspose.Words.ImportFormatModeimportFormatOptions: Aspose.Words.ImportFormatOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../) | The document to append. |
| importFormatMode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |
| importFormatOptions | [ImportFormatOptions](../../importformatoptions/) | Allows to specify options that affect formatting of a result document. |

## Examples

Shows how to append a document to the end of another document.

```js
const srcDoc = new aw.Document();
srcDoc.firstSection.body.appendParagraph("Source document text. ");

const dstDoc = new aw.Document();
dstDoc.firstSection.body.appendParagraph("Destination document text. ");

// Append the source document to the destination document while preserving its formatting,
// then save the source document to the local file system.
dstDoc.appendDocument(srcDoc, aw.ImportFormatMode.KeepSourceFormatting);

dstDoc.save(base.artifactsDir + "Document.AppendDocument.docx");
```

Shows how to append all the documents in a folder to the end of a template document.

```js
const dstDoc = new aw.Document();
const builder = new aw.DocumentBuilder(dstDoc);
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.writeln("Template Document");
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Normal;
builder.writeln("Some content here");
// Append all unencrypted documents with the .doc extension
// from our local file system directory to the base document.
const docFiles = [];
fs.readdirSync(base.myDir).forEach(file => {
  if (file.endsWith('.doc')) {
    docFiles.push(base.myDir + file); 
  }
});
for (var i = 0; i < docFiles.length; i++) {
  const fileName = docFiles[i];
  const info = aw.FileFormatUtil.detectFileFormat(fileName);
  if (info.isEncrypted)
      continue;
  const srcDoc = new aw.Document(fileName);
  dstDoc.appendDocument(srcDoc, aw.ImportFormatMode.UseDestinationStyles);
}
dstDoc.save(base.artifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

Shows how to manage list style clashes while appending a document.

```js
// Load a document with text in a custom style and clone it.
let srcDoc = new aw.Document(base.myDir + "Custom list numbering.docx");
let dstDoc = srcDoc.clone();

// We now have two documents, each with an identical style named "CustomStyle".
// Change the text color for one of the styles to set it apart from the other.
dstDoc.styles.at("CustomStyle").font.color = "#8B0000";

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
let options = new aw.ImportFormatOptions();
options.keepSourceNumbering = keepSourceNumbering;

// Joining two documents that have different styles that share the same name causes a style clash.
// We can specify an import format mode while appending documents to resolve this clash.
dstDoc.appendDocument(srcDoc, aw.ImportFormatMode.KeepDifferentStyles, options);
dstDoc.updateListLabels();

dstDoc.save(base.artifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

Shows how to manage list style clashes while inserting a document.

```js
let dstDoc = new aw.Document();
let builder = new aw.DocumentBuilder(dstDoc);
builder.insertBreak(aw.BreakType.ParagraphBreak);

dstDoc.lists.add(aw.Lists.ListTemplate.NumberDefault);
let list = dstDoc.lists.at(0);

builder.listFormat.list = list;

for (let i = 1; i <= 15; i++)
  builder.write(`List Item ${i}\n`);

let attachDoc = dstDoc.clone();

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
let importOptions = new aw.ImportFormatOptions();
importOptions.keepSourceNumbering = keepSourceNumbering;

builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.insertDocument(attachDoc, aw.ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.save(base.artifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Shows how to manage list style clashes while appending a clone of a document to itself.

```js
let srcDoc = new aw.Document(base.myDir + "List item.docx");
let dstDoc = new aw.Document(base.myDir + "List item.docx");

// If there is a clash of list styles, apply the list format of the source document.
// Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
// Set the "KeepSourceNumbering" property to "true" import all clashing
// list style numbering with the same appearance that it had in the source document.
let builder = new aw.DocumentBuilder(dstDoc);
builder.moveToDocumentEnd();
builder.insertBreak(aw.BreakType.SectionBreakNewPage);

let options = new aw.ImportFormatOptions();
options.keepSourceNumbering = keepSourceNumbering;
builder.insertDocument(srcDoc, aw.ImportFormatMode.KeepSourceFormatting, options);

dstDoc.updateListLabels();
```

## See Also

* module [Aspose.Words](../../)
* class [Document](../)

