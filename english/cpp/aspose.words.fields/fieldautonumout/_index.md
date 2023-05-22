---
title: Aspose::Words::Fields::FieldAutoNumOut class
linktitle: FieldAutoNumOut
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldAutoNumOut class. Implements the AUTONUMOUT field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.fields/fieldautonumout/
---
## FieldAutoNumOut class


Implements the AUTONUMOUT field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldAutoNumOut : public Aspose::Words::Fields::Field
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
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to number paragraphs using AUTONUMOUT fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// AUTONUMOUT fields display a number that increments at each AUTONUMOUT field.
// Unlike AUTONUM fields, AUTONUMOUT fields use the outline numbering scheme,
// which we can define in Microsoft Word via Format -> Bullets & Numbering -> "Outline Numbered".
// This allows us to automatically number items like a numbered list.
// LISTNUM fields are a newer alternative to AUTONUMOUT fields.
// This field will display "1.".
builder->InsertField(FieldType::FieldAutoNumOutline, true);
builder->Writeln(u"\tParagraph 1.");

// This field will display "2.".
builder->InsertField(FieldType::FieldAutoNumOutline, true);
builder->Writeln(u"\tParagraph 2.");

for (auto field : System::IterateOver<FieldAutoNumOut>(
         doc->get_Range()->get_Fields()->LINQ_Where([](SharedPtr<Field> f) { return f->get_Type() == FieldType::FieldAutoNumOutline; })))
{
    ASSERT_EQ(u" AUTONUMOUT ", field->GetFieldCode());
}

doc->Save(ArtifactsDir + u"Field.AUTONUMOUT.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
