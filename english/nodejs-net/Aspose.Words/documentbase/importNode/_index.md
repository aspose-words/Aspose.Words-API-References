---
title: DocumentBase.importNode method
linktitle: importNode method
articleTitle: importNode method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DocumentBase.importNode method"
type: docs
weight: 100
url: /nodejs-net/aspose.words/documentbase/importNode/
---

## importNode(srcNode, isImportChildren) {#node_boolean}

Imports a node from another document to the current document.




```js
importNode(srcNode: Aspose.Words.Node, isImportChildren: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../node/) | The node being imported. |
| isImportChildren | boolean | ``true`` to import all child nodes recursively; otherwise, ``false``. |

### Remarks

This method uses the [ImportFormatMode.UseDestinationStyles](../../importformatmode/#UseDestinationStyles) option to resolve formatting.

Importing a node creates a copy of the source node belonging to the importing document. 
The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported.
During import, document-specific properties such as references to styles and lists are translated
from the original to the importing document. After the node was imported, it can be inserted
into the appropriate place in the document using [CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node) or 
[CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node).

If the source node already belongs to the destination document, then simply a deep clone
of the source node is created.




### Returns

The cloned node that belongs to the current document.


## importNode(srcNode, isImportChildren, importFormatMode) {#node_boolean_importformatmode}

Imports a node from another document to the current document with an option to control formatting.




```js
importNode(srcNode: Aspose.Words.Node, isImportChildren: boolean, importFormatMode: Aspose.Words.ImportFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../node/) | The node to imported. |
| isImportChildren | boolean | ``true`` to import all child nodes recursively; otherwise, ``false``. |
| importFormatMode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |

### Remarks

This overload is useful to control how styles and list formatting are imported.

Importing a node creates a copy of the source node belonging to the importing document. 
The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported.
During import, document-specific properties such as references to styles and lists are translated
from the original to the importing document. After the node was imported, it can be inserted
into the appropriate place in the document using [CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node) or 
[CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node).

If the source node already belongs to the destination document, then simply a deep clone
of the source node is created.




### Returns

The cloned, imported node. The node belongs to the destination document, but has no parent.


## Examples

Shows how to import a node from one document to another.

```js
let srcDoc = new aw.Document();
let dstDoc = new aw.Document();

srcDoc.firstSection.body.firstParagraph.appendChild(
  new aw.Run(srcDoc, "Source document first paragraph text."));
dstDoc.firstSection.body.firstParagraph.appendChild(
  new aw.Run(dstDoc, "Destination document first paragraph text."));

// Every node has a parent document, which is the document that contains the node.
// Inserting a node into a document that the node does not belong to will throw an exception.
expect(srcDoc.firstSection.document).not.toEqual(dstDoc);
expect(() => { dstDoc.appendChild(srcDoc.firstSection); }).toThrow("The newChild was created from a different document than the one that created this node.");

// Use the ImportNode method to create a copy of a node, which will have the document
// that called the ImportNode method set as its new owner document.
let importedSection = dstDoc.importNode(srcDoc.firstSection, true).asSection();

expect(importedSection.document.referenceEquals(dstDoc)).toBeTruthy();

// We can now insert the node into the document.
dstDoc.appendChild(importedSection);

expect(dstDoc.toString(aw.SaveFormat.Text)).toEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n");
```

Shows how to import node from source document to destination document with specific options.

```js
// Create two documents and add a character style to each document.
// Configure the styles to have the same name, but different text formatting.
let srcDoc = new aw.Document();
let srcStyle = srcDoc.styles.add(aw.StyleType.Character, "My style");
srcStyle.font.name = "Courier New";
let srcBuilder = new aw.DocumentBuilder(srcDoc);
srcBuilder.font.style = srcStyle;
srcBuilder.writeln("Source document text.");

let dstDoc = new aw.Document();
let dstStyle = dstDoc.styles.add(aw.StyleType.Character, "My style");
dstStyle.font.name = "Calibri";
let dstBuilder = new aw.DocumentBuilder(dstDoc);
dstBuilder.font.style = dstStyle;
dstBuilder.writeln("Destination document text.");

// Import the Section from the destination document into the source document, causing a style name collision.
// If we use destination styles, then the imported source text with the same style name
// as destination text will adopt the destination style.
let importedSection = dstDoc.importNode(srcDoc.firstSection, true, aw.ImportFormatMode.UseDestinationStyles).asSection();
expect(importedSection.body.paragraphs.at(0).runs.at(0).getText().trim()).toEqual("Source document text.");
expect(dstDoc.styles.at("My style_0")).toBe(null);
expect(importedSection.body.firstParagraph.runs.at(0).font.name).toEqual(dstStyle.font.name);
expect(importedSection.body.firstParagraph.runs.at(0).font.styleName).toEqual(dstStyle.name);

// If we use ImportFormatMode.KeepDifferentStyles, the source style is preserved,
// and the naming clash resolves by adding a suffix.
dstDoc.importNode(srcDoc.firstSection, true, aw.ImportFormatMode.KeepDifferentStyles);
expect(dstDoc.styles.at("My style").font.name).toEqual(dstStyle.font.name);
expect(dstDoc.styles.at("My style_0").font.name).toEqual(srcStyle.font.name);
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBase](../)
* class [NodeImporter](../../nodeimporter/)
* enum [ImportFormatMode](../../importformatmode/)

