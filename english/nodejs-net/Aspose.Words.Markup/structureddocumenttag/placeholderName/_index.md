---
title: StructuredDocumentTag.placeholderName property
linktitle: placeholderName property
articleTitle: placeholderName property
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.placeholderName property. Gets or sets Name of the [BuildingBlock](../../../aspose.words/buildingblock/) containing placeholder text."
type: docs
weight: 240
url: /nodejs-net/aspose.words.markup/structureddocumenttag/placeholderName/
---

## StructuredDocumentTag.placeholderName property

Gets or sets Name of the [BuildingBlock](../../../aspose.words/buildingblock/) containing placeholder text.




```js
get placeholderName(): string
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if BuildingBlock with this name [BuildingBlock.name](../../../aspose.words/buildingblock/name/) is not present in [Document.glossaryDocument](../../../aspose.words/document/glossaryDocument/). |

### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```js
let doc = new aw.Document();

// Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
// The contents that it will display by default are a "Click here to enter text." prompt.
let tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Inline);

// We can get the tag to display the contents of a building block instead of the default text.
// First, add a building block with contents to the glossary document.
let glossaryDoc = doc.glossaryDocument;

let substituteBlock = new aw.BuildingBlocks.BuildingBlock(glossaryDoc);
substituteBlock.name = "Custom Placeholder";
substituteBlock.appendChild(new aw.Section(glossaryDoc));
substituteBlock.firstSection.appendChild(new aw.Body(glossaryDoc));
substituteBlock.firstSection.body.appendParagraph("Custom placeholder text.");

glossaryDoc.appendChild(substituteBlock);

// Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
tag.placeholderName = "Custom Placeholder";

// If "PlaceholderName" refers to an existing block in the parent document's glossary document,
// we will be able to verify the building block via the "Placeholder" property.
expect(tag.placeholder.referenceEquals(substituteBlock)).toBe(true);

// Set the "IsShowingPlaceholderText" property to "true" to treat the
// structured document tag's current contents as placeholder text.
// This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
// Set the "IsShowingPlaceholderText" property to "false" to get the
// structured document tag to treat its contents as text that a user has already entered.
// Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
tag.isShowingPlaceholderText = isShowingPlaceholderText;

let builder = new aw.DocumentBuilder(doc);
builder.insertNode(tag);

doc.save(base.artifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

