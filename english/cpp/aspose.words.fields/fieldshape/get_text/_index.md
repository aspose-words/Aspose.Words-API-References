---
title: get_Text
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the text to retrieve.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldshape/get_text/
---
## FieldShape::get_Text method


Gets or sets the text to retrieve.

```cpp
System::String Aspose::Words::Fields::FieldShape::get_Text()
```


## Examples



Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
// but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
// The following field will display ".1", the RTL equivalent of list number "1.".
auto field = System::DynamicCast<FieldBidiOutline>(builder->InsertField(FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
builder->InsertField(FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Set the horizontal text alignment for every paragraph in the document to RTL.
for (const auto& para : System::IterateOver<Paragraph>(doc->GetChildNodes(NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
// Otherwise, they will display "###".
doc->Save(ArtifactsDir + u"Field.BIDIOUTLINE.docx");
```


Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading. 
```cpp
// Open a document that was created in Microsoft Word 2003.
auto doc = MakeObject<Document>(MyDir + u"Legacy fields.doc");

// If we open the Word document and press Alt+F9, we will see a SHAPE and an EMBED field.
// A SHAPE field is the anchor/canvas for an AutoShape object with the "In line with text" wrapping style enabled.
// An EMBED field has the same function, but for an embedded object,
// such as a spreadsheet from an external Excel document.
// However, these fields will not appear in the document's Fields collection.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// These fields are supported only by old versions of Microsoft Word.
// The document loading process will convert these fields into Shape objects,
// which we can access in the document's node collection.
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// The first Shape node corresponds to the SHAPE field in the input document,
// which is the inline canvas for the AutoShape.
auto shape = System::DynamicCast<Shape>(shapes->idx_get(0));
ASSERT_EQ(ShapeType::Image, shape->get_ShapeType());

// The second Shape node is the AutoShape itself.
shape = System::DynamicCast<Shape>(shapes->idx_get(1));
ASSERT_EQ(ShapeType::Can, shape->get_ShapeType());

// The third Shape is what was the EMBED field that contained the external spreadsheet.
shape = System::DynamicCast<Shape>(shapes->idx_get(2));
ASSERT_EQ(ShapeType::OleObject, shape->get_ShapeType());
```

## See Also

* Class [FieldShape](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
