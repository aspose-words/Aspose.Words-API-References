---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Manage FieldShape text easily—get or set values effortlessly for seamless data retrieval and enhanced functionality in your applications.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Gets or sets the text to retrieve.

```csharp
public string Text { get; set; }
```

## Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
// but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
// The following field will display ".1", the RTL equivalent of list number "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.That(field.GetFieldCode(), Is.EqualTo(" BIDIOUTLINE "));

// Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Set the horizontal text alignment for every paragraph in the document to RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
// Otherwise, they will display "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

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

* class [FieldShape](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
