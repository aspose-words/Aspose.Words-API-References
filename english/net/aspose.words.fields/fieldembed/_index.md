---
title: FieldEmbed Class
linktitle: FieldEmbed
articleTitle: FieldEmbed
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldEmbed class for seamless EMBED field implementation, enhancing document functionality and versatility.
type: docs
weight: 2250
url: /net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

Implements the EMBED field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldEmbed : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldEmbed](fieldembed/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Examples

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```csharp
// Open a document that was created in Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// If we open the Word document and press Alt+F9, we will see a SHAPE and an EMBED field.
// A SHAPE field is the anchor/canvas for an AutoShape object with the "In line with text" wrapping style enabled.
// An EMBED field has the same function, but for an embedded object,
// such as a spreadsheet from an external Excel document.
// However, these fields will not appear in the document's Fields collection.
Assert.That(doc.Range.Fields.Count, Is.EqualTo(0));

// These fields are supported only by old versions of Microsoft Word.
// The document loading process will convert these fields into Shape objects,
// which we can access in the document's node collection.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.That(shapes.Count, Is.EqualTo(3));

// The first Shape node corresponds to the SHAPE field in the input document,
// which is the inline canvas for the AutoShape.
Shape shape = (Shape)shapes[0];
Assert.That(shape.ShapeType, Is.EqualTo(ShapeType.Image));

// The second Shape node is the AutoShape itself.
shape = (Shape)shapes[1];
Assert.That(shape.ShapeType, Is.EqualTo(ShapeType.Can));

// The third Shape is what was the EMBED field that contained the external spreadsheet.
shape = (Shape)shapes[2];
Assert.That(shape.ShapeType, Is.EqualTo(ShapeType.OleObject));
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
