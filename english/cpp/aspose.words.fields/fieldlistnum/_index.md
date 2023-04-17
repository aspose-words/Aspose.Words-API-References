---
title: Aspose::Words::Fields::FieldListNum class
linktitle: FieldListNum
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldListNum class. Implements the LISTNUM field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 64000
url: /cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


Implements the LISTNUM field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_HasListName](./get_haslistname/)() | Returns a value indicating whether the name of an abstract numbering definition is provided by the field's code. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_ListLevel](./get_listlevel/)() | Gets or sets the level in the list, overriding the default behavior of the field. |
| [get_ListName](./get_listname/)() | Gets or sets the name of the abstract numbering definition used for the numbering. |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_StartingNumber](./get_startingnumber/)() | Gets or sets the starting value for this field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/). |
| [set_ListName](./set_listname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to number paragraphs with LISTNUM fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// LISTNUM fields display a number that increments at each LISTNUM field.
// These fields also have a variety of options that allow us to use them to emulate numbered lists.
auto field = System::DynamicCast<FieldListNum>(builder->InsertField(FieldType::FieldListNum, true));

// Lists start counting at 1 by default, but we can set this number to a different value, such as 0.
// This field will display "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// LISTNUM fields maintain separate counts for each list level.
// Inserting a LISTNUM field in the same paragraph as another LISTNUM field
// increases the list level instead of the count.
// The next field will continue the count we started above and display a value of "1" at list level 1.
builder->InsertField(FieldType::FieldListNum, true);

// This field will start a count at list level 2. It will display a value of "1".
builder->InsertField(FieldType::FieldListNum, true);

// This field will start a count at list level 3. It will display a value of "1".
// Different list levels have different formatting,
// so these fields combined will display a value of "1)a)i)".
builder->InsertField(FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// The next LISTNUM field that we insert will continue the count at the list level
// that the previous LISTNUM field was on.
// We can use the "ListLevel" property to jump to a different list level.
// If this LISTNUM field stayed on list level 3, it would display "ii)",
// but, since we have moved it to list level 2, it carries on the count at that level and displays "b)".
field = System::DynamicCast<FieldListNum>(builder->InsertField(FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// We can set the ListName property to get the field to emulate a different AUTONUM field type.
// "NumberDefault" emulates AUTONUM, "OutlineDefault" emulates AUTONUMOUT,
// and "LegalDefault" emulates AUTONUMLGL fields.
// The "OutlineDefault" list name with 1 as the starting number will result in displaying "I.".
field = System::DynamicCast<FieldListNum>(builder->InsertField(FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// The ListName does not carry over from the previous field, so we will need to set it for each new field.
// This field continues the count with the different list name and displays "II.".
field = System::DynamicCast<FieldListNum>(builder->InsertField(FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.LISTNUM.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
