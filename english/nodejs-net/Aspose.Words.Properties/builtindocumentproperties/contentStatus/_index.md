---
title: BuiltInDocumentProperties.contentStatus property
linktitle: contentStatus property
articleTitle: contentStatus property
second_title: Aspose.Words for NodeJs
description: "BuiltInDocumentProperties.contentStatus property. Gets or sets the content status of the document."
type: docs
weight: 80
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/contentStatus/
---

## BuiltInDocumentProperties.contentStatus property

Gets or sets the content status of the document.


```js
get contentStatus(): string
```

### Examples

Shows how to work with document properties in the "Content" category.

```js
test('Content', () => {
  let doc = new aw.Document(base.myDir + "Paragraphs.docx");
  let properties = doc.builtInDocumentProperties;

  // By using built in properties,
  // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
  // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
  // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
  // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
  // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

  // The "Pages" property stores the page count of the document. 
  expect(properties.pages).toEqual(6);

  // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
  // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
  expect(properties.words).toEqual(1054);
  expect(properties.characters).toEqual(6009);
  expect(properties.charactersWithSpaces).toEqual(7049);
  doc.updateWordCount();

  expect(properties.words).toEqual(1035);
  expect(properties.characters).toEqual(6026);
  expect(properties.charactersWithSpaces).toEqual(7041);

  // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
  let lineCounter = new LineCounter(doc);
  properties.lines = lineCounter.getLineCount();

  expect(properties.lines).toEqual(142);

  // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
  properties.paragraphs = doc.getChildNodes(aw.NodeType.Paragraph, true).count;
  expect(properties.paragraphs).toEqual(29);

  // Get an estimate of the file size of our document via the "Bytes" built-in property.
  expect(properties.bytes).toEqual(20310);

  // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
  doc.attachedTemplate = base.myDir + "Business brochure.dotx";

  expect(properties.template).toEqual("Normal");

  properties.template = doc.attachedTemplate;

  // "ContentStatus" is a descriptive built-in property.
  properties.contentStatus = "Draft";

  // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
  expect(properties.contentType).toEqual('');

  // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
  expect(properties.linksUpToDate).toEqual(false);

  doc.save(base.artifactsDir + "DocumentProperties.content.docx");
});
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [BuiltInDocumentProperties](../)

