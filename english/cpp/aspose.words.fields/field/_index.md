---
title: Field
second_title: Aspose.Words for C++ API Reference
description: Represents a Microsoft Word document field. To learn more, visit the documentation article.
type: docs
weight: 53
url: /cpp/aspose.words.fields/field/
---
## Field class


Represents a Microsoft Word document field. To learn more, visit the documentation article.

```cpp
class Field : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](./get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](./get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](./get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](./get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](./get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](./get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](./get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](./get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](./get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](./get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](./get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](./getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](./getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](./remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](./set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/). |
| [set_Result](./set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](./get_result/). |
| [Unlink](./unlink/)() | Performs the field unlink. |
| [Update](./update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](./update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## Remarks


A field in a Word document is a complex structure consisting of multiple nodes that include field start, field code, field separator, field result and field end. [Fields](../) can be nested, contain rich content and span multiple paragraphs or sections in a document. The [Field](./) class is a "facade" object that provides properties and methods that allow to work with a field as a single object.

The [Start](./get_start/), [Separator](./get_separator/) and [End](./get_end/) properties point to the field start, separator and end nodes of the field respectively.

The content between the field start and separator is the field code. The content between the field separator and field end is the field result. The field code typically consists of one or more [Run](../../aspose.words/run/) objects that specify instructions. The processing application is expected to execute the field code to calculate the field result.

The process of calculating field results is called the field update. Aspose.Words can update field results of most of the field types in exactly the same way as Microsoft Word does it. Most notably, Aspose.Words can calculate results of even the most complex formula fields. To calculate the field result of a single field use the [Update](./update/) method. To update fields in the whole document use [UpdateFields](../../aspose.words/document/updatefields/).

You can get the plain text version of the field code using the [GetFieldCode()](./getfieldcode/) method. You can get and set the plain text version of the field result using the [Result](./get_result/) property. Both the field code and field result can contain complex content, such as nested fields, paragraphs, shapes, tables and in this case you might want to work with the field nodes directly if you need more control.

You do not create instances of the [Field](./) class directly. To create a new field use the [InsertField()](../) method.

## Examples



Shows how to insert a field into a document using a field code. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// This overload of the InsertField method automatically updates inserted fields.
ASSERT_LE(System::Math::Abs((System::DateTime::Parse(field->get_Result()) - System::DateTime::get_Today()).get_Hours()), 24);
```

## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
