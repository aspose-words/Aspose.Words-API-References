---
title: Enum NodeType
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.NodeType enum. Specifies the type of a Word document node in C#
type: docs
weight: 4020
url: /net/aspose.words/nodetype/
---
## NodeType enumeration

Specifies the type of a Word document node.

```csharp
public enum NodeType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Any | `0` | Indicates all node types. Allows to select all children. |
| Document | `1` | A [`Document`](../document/) object that, as the root of the document tree, provides access to the entire Word document. |
| Section | `2` | A [`Section`](../section/) object that corresponds to one section in a Word document. |
| Body | `3` | A [`Body`](../body/) object that contains the main text of a section (main text story). |
| HeaderFooter | `4` | A [`HeaderFooter`](../headerfooter/) object that contains text of a particular header or footer inside a section. |
| Table | `5` | A [`Table`](../../aspose.words.tables/table/) object that represents a table in a Word document. |
| Row | `6` | A row of a table. |
| Cell | `7` | A cell of a table row. |
| Paragraph | `8` | A paragraph of text. |
| BookmarkStart | `9` | A beginning of a bookmark marker. |
| BookmarkEnd | `10` | An end of a bookmark marker. |
| EditableRangeStart | `11` | A beginning of an editable range. |
| EditableRangeEnd | `12` | An end of an editable range. |
| MoveFromRangeStart | `13` | A beginning of an MoveFrom range. |
| MoveFromRangeEnd | `14` | An end of an MoveFrom range. |
| MoveToRangeStart | `15` | A beginning of an MoveTo range. |
| MoveToRangeEnd | `16` | An end of an MoveTo range. |
| GroupShape | `17` | A group of shapes, images, OLE objects or other group shapes. |
| Shape | `18` | A drawing object, such as an OfficeArt shape, image or an OLE object. |
| Comment | `19` | A comment in a Word document. |
| Footnote | `20` | A footnote or endnote in a Word document. |
| Run | `21` | A run of text. |
| FieldStart | `22` | A special character that designates the start of a Word field. |
| FieldSeparator | `23` | A special character that separates the field code from the field result. |
| FieldEnd | `24` | A special character that designates the end of a Word field. |
| FormField | `25` | A form field. |
| SpecialChar | `26` | A special character that is not one of the more specific special character types. |
| SmartTag | `27` | A smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph |
| StructuredDocumentTag | `28` | Allows to define customer-specific information and its means of presentation. |
| StructuredDocumentTagRangeStart | `29` | A start of **ranged** structured document tag which accepts multi-sections content. |
| StructuredDocumentTagRangeEnd | `30` | A end of **ranged** structured document tag which accepts multi-sections content. |
| GlossaryDocument | `31` | A glossary document within the main document. |
| BuildingBlock | `32` | A building block within a glossary document (e.g. glossary document entry). |
| CommentRangeStart | `33` | A marker node that represents the start of a commented range. |
| CommentRangeEnd | `34` | A marker node that represents the end of a commented range. |
| OfficeMath | `35` | An Office Math object. Can be equation, function, matrix or one of other mathematical objects. Can be a collection of mathematical object and also can contain some non-mathematical objects such as runs of text. |
| SubDocument | `36` | A subdocument node which is a link to another document. |
| System | `37` | Reserved for internal use by Aspose.Words. |
| Null | `38` | Reserved for internal use by Aspose.Words. |

## Examples

Shows how to traverse through a composite node's collection of child nodes.

```csharp
Document doc = new Document();

// Add two runs and one shape as child nodes to the first paragraph of this document.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
    }
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
