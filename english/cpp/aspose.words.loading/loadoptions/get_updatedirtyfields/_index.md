---
title: get_UpdateDirtyFields
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to update the fields with the dirty attribute.
type: docs
weight: 196
url: /cpp/aspose.words.loading/loadoptions/get_updatedirtyfields/
---
## LoadOptions::get_UpdateDirtyFields method


Specifies whether to update the fields with the **dirty** attribute.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields() const
```


## Examples



Shows how to use special property for updating field result. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Give the document's built-in "Author" property value, and then display it with a field.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::DynamicCast<FieldAuthor>(builder->InsertField(FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Update the property. The field still displays the old value.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Since the field's value is out of date, we can mark it as "dirty".
// This value will stay out of date until we update the field manually with the Field.Update() method.
field->set_IsDirty(true);

{
    auto docStream = MakeObject<System::IO::MemoryStream>();
    // If we save without calling an update method,
    // the field will keep displaying the out of date value in the output document.
    doc->Save(docStream, SaveFormat::Docx);

    // The LoadOptions object has an option to update all fields
    // marked as "dirty" when loading the document.
    auto options = MakeObject<Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = MakeObject<Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::DynamicCast<FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // Updating dirty fields like this automatically set their "IsDirty" flag to false.
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
