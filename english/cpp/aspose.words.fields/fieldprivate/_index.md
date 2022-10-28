---
title: FieldPrivate
second_title: Aspose.Words for C++ API Reference
description: Implements the PRIVATE field.
type: docs
weight: 1054
url: /cpp/aspose.words.fields/fieldprivate/
---
## FieldPrivate class


Implements the PRIVATE field.

```cpp
class FieldPrivate : public Aspose::Words::Fields::Field
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples




Shows how to process PRIVATE fields. 
```cpp
void FieldPrivate_()
{
    // Open a Corel WordPerfect document which we have converted to .docx format.
    auto doc = MakeObject<Document>(MyDir + u"Field sample - PRIVATE.docx");

    // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
    // Microsoft Word preserves PRIVATE fields during load/save operations,
    // but provides no functionality for them.
    auto field = System::DynamicCast<FieldPrivate>(doc->get_Range()->get_Fields()->idx_get(0));

    ASSERT_EQ(u" PRIVATE \"My value\" ", field->GetFieldCode());
    ASSERT_EQ(FieldType::FieldPrivate, field->get_Type());

    // We can also insert PRIVATE fields using a document builder.
    auto builder = MakeObject<DocumentBuilder>(doc);
    builder->InsertField(FieldType::FieldPrivate, true);

    // These fields are not a viable way of protecting sensitive information.
    // Unless backward compatibility with older versions of WordPerfect is essential,
    // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
    ASSERT_EQ(2, doc->get_Range()->get_Fields()->get_Count());

    auto remover = MakeObject<ExField::FieldPrivateRemover>();
    doc->Accept(remover);

    ASSERT_EQ(2, remover->GetFieldsRemovedCount());
    ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());
}

class FieldPrivateRemover : public DocumentVisitor
{
public:
    FieldPrivateRemover() : mFieldsRemovedCount(0)
    {
        mFieldsRemovedCount = 0;
    }

    int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    VisitorAction VisitFieldEnd(SharedPtr<FieldEnd> fieldEnd) override
    {
        if (fieldEnd->get_FieldType() == FieldType::FieldPrivate)
        {
            fieldEnd->GetField()->Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction::Continue;
    }

private:
    int mFieldsRemovedCount;
};
```

