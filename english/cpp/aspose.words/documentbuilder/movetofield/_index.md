---
title: Aspose::Words::DocumentBuilder::MoveToField method
linktitle: MoveToField
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::MoveToField method. Moves the cursor to a field in the document in C++.'
type: docs
weight: 56000
url: /cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


Moves the cursor to a field in the document.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| Parameter | Type | Description |
| --- | --- | --- |
| field | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | The field to move the cursor to. |
| isAfter | bool | When **true**, moves the cursor to be after the field end. When **false**, moves the cursor to be before the field start. |

## Examples



Shows how to move a document builder's node insertion point cursor to a specific field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a field using the DocumentBuilder and add a run of text after it.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// The builder's cursor is currently at end of the document.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Move the cursor to the field while specifying whether to place that cursor before or after the field.
builder->MoveToField(field, moveCursorToAfterTheField);

// Note that the cursor is outside of the field in both cases.
// This means that we cannot edit the field using the builder like this.
// To edit a field, we can use the builder's MoveTo method on a field's FieldStart
// or FieldSeparator node to place the cursor inside.
if (moveCursorToAfterTheField)
{
    ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));
    builder->Write(u" Text immediately after the field.");

    ASSERT_EQ(u"\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", doc->GetText().Trim());
}
else
{
    ASPOSE_ASSERT_EQ(field->get_Start(), builder->get_CurrentNode());
    builder->Write(u"Text immediately before the field. ");

    ASSERT_EQ(u"Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", doc->GetText().Trim());
}
```

## See Also

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
