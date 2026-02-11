---
title: NodeType enumeration
linktitle: NodeType enumeration
articleTitle: NodeType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.NodeType enumeration. Specifies the type of a Word document node."
type: docs
weight: 910
url: /nodejs-net/aspose.words/nodetype/
---

## NodeType enumeration

Specifies the type of a Word document node.


### Members

| Name | Description |
| --- | --- |
| Any | Indicates all node types. Allows to select all children. |
| Document | A [Document](../document/) object that, as the root of the document tree, provides access to the entire Word document. |
| Section | A [Section](../section/) object that corresponds to one section in a Word document. |
| Body | A [Body](../body/) object that contains the main text of a section (main text story). |
| HeaderFooter | A [HeaderFooter](../headerfooter/) object that contains text of a particular header or footer inside a section. |
| Table | A [Table](../table/) object that represents a table in a Word document. |
| Row | A row of a table. |
| Cell | A cell of a table row. |
| Paragraph | A paragraph of text. |
| BookmarkStart | A beginning of a bookmark marker. |
| BookmarkEnd | An end of a bookmark marker. |
| EditableRangeStart | A beginning of an editable range. |
| EditableRangeEnd | An end of an editable range. |
| MoveFromRangeStart | A beginning of an MoveFrom range. |
| MoveFromRangeEnd | An end of an MoveFrom range. |
| MoveToRangeStart | A beginning of an MoveTo range. |
| MoveToRangeEnd | An end of an MoveTo range. |
| GroupShape | A group of shapes, images, OLE objects or other group shapes. |
| Shape | A drawing object, such as an OfficeArt shape, image or an OLE object. |
| Comment | A comment in a Word document. |
| Footnote | A footnote or endnote in a Word document. |
| Run | A run of text. |
| FieldStart | A special character that designates the start of a Word field. |
| FieldSeparator | A special character that separates the field code from the field result. |
| FieldEnd | A special character that designates the end of a Word field. |
| FormField | A form field. |
| SpecialChar | A special character that is not one of the more specific special character types. |
| SmartTag | A smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph |
| StructuredDocumentTag | Allows to define customer-specific information and its means of presentation. |
| StructuredDocumentTagRangeStart | A start of **ranged** structured document tag which accepts multi-sections content. |
| StructuredDocumentTagRangeEnd | A end of **ranged** structured document tag which accepts multi-sections content. |
| GlossaryDocument | A glossary document within the main document. |
| BuildingBlock | A building block within a glossary document (e.g. glossary document entry). |
| CommentRangeStart | A marker node that represents the start of a commented range. |
| CommentRangeEnd | A marker node that represents the end of a commented range. |
| OfficeMath | An Office Math object. Can be equation, function, matrix or one of other mathematical objects. Can be a collection of mathematical object and also can contain some non-mathematical objects such as runs of text. |
| SubDocument | A subdocument node which is a link to another document. |
| System | Reserved for internal use by Aspose.Words. |
| Null | Reserved for internal use by Aspose.Words. |

### Examples

Shows how to traverse through a composite node's collection of child nodes.

```js
let doc = new aw.Document();

// Add two runs and one shape as child nodes to the first paragraph of this document.
let paragraph = doc.getParagraph(0, true);
paragraph.appendChild(new aw.Run(doc, "Hello world! "));

let shape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Rectangle);
shape.width = 200;
shape.height = 200;
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape.customNodeId = 100;
shape.wrapType = aw.Drawing.WrapType.Inline;
paragraph.appendChild(shape);

paragraph.appendChild(new aw.Run(doc, "Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
let children = paragraph.getChildNodes(aw.NodeType.Any, false);

expect(paragraph.getChildNodes(aw.NodeType.Any, false).count).toEqual(3);

for (let child of children)
  switch (child.nodeType)
  {
    case aw.NodeType.Run:
      console.log("Run contents:");
      console.log(`\t\"${child.getText().trim()}\"`);
      break;
    case aw.NodeType.Shape:
      let childShape = child.asShape();
      console.log("Shape:");
      console.log(`\t${childShape.shapeType}, ${childShape.width}x${childShape.height}`);
      expect(shape.customNodeId).toEqual(100);
      break;
  }
```

### See Also

* module [Aspose.Words](../)

