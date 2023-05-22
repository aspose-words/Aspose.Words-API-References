---
title: Aspose::Words::Fields::FieldShape class
linktitle: FieldShape
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldShape class. Implements the SHAPE field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 93000
url: /cpp/aspose.words.fields/fieldshape/
---
## FieldShape class


Implements the SHAPE field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldShape : public Aspose::Words::Fields::Field
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_Text](./get_text/)() | Gets or sets the text to retrieve. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_Text](./set_text/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldShape::get_Text](./get_text/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
// but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
// The following field will display ".1", the RTL equivalent of list number "1.".
auto field = System::ExplicitCast<FieldBidiOutline>(builder->InsertField(FieldType::FieldBidiOutline, true));
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
auto shape = System::ExplicitCast<Shape>(shapes->idx_get(0));
ASSERT_EQ(ShapeType::Image, shape->get_ShapeType());

// The second Shape node is the AutoShape itself.
shape = System::ExplicitCast<Shape>(shapes->idx_get(1));
ASSERT_EQ(ShapeType::Can, shape->get_ShapeType());

// The third Shape is what was the EMBED field that contained the external spreadsheet.
shape = System::ExplicitCast<Shape>(shapes->idx_get(2));
ASSERT_EQ(ShapeType::OleObject, shape->get_ShapeType());
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
