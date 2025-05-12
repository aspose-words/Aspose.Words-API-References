---
title: StructuredDocumentTag.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.clear method. Clears contents of this structured document tag and displays a placeholder if it is defined."
type: docs
weight: 330
url: /nodejs-net/aspose.words.markup/structureddocumenttag/clear/
---

## clear() {#default}

Clears contents of this structured document tag and displays a placeholder if it is defined.


```js
clear()
```

### Remarks

It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [StructuredDocumentTag.xmlMapping](../xmlMapping/)
property), the referenced XML node is cleared.




### Examples

Shows how to delete contents of structured document tag elements.

```js
let doc = new aw.Document();

// Create a plain text structured document tag, and then append it to the document.
let tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Block);
doc.firstSection.body.appendChild(tag);

// This structured document tag, which is in the form of a text box, already displays placeholder text.
expect(tag.getText().trim()).toEqual("Click here to enter text.");
expect(tag.isShowingPlaceholderText).toEqual(true);

// Create a building block with text contents.
let glossaryDoc = doc.glossaryDocument;
let substituteBlock = new aw.BuildingBlocks.BuildingBlock(glossaryDoc);
substituteBlock.name = "My placeholder";
substituteBlock.appendChild(new aw.Section(glossaryDoc));
substituteBlock.firstSection.ensureMinimum();
substituteBlock.firstSection.body.firstParagraph.appendChild(new aw.Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.appendChild(substituteBlock);

// Set the structured document tag's "PlaceholderName" property to our building block's name to get
// the structured document tag to display the contents of the building block in place of the original default text.
tag.placeholderName = "My placeholder";

expect(tag.getText().trim()).toEqual("Custom placeholder text.");
expect(tag.isShowingPlaceholderText).toEqual(true);

// Edit the text of the structured document tag and hide the placeholder text.
let run = tag.getChild(aw.NodeType.Run, 0, true).asRun();
run.text = "New text.";
tag.isShowingPlaceholderText = false;

expect(tag.getText().trim()).toEqual("New text.");

// Use the "Clear" method to clear this structured document tag's contents and display the placeholder again.
tag.clear();

expect(tag.isShowingPlaceholderText).toEqual(true);
expect(tag.getText().trim()).toEqual("Custom placeholder text.");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

