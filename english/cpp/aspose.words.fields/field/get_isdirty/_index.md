---
title: Aspose::Words::Fields::Field::get_IsDirty method
linktitle: get_IsDirty
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::Field::get_IsDirty method. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.fields/field/get_isdirty/
---
## Field::get_IsDirty method


Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

```cpp
bool Aspose::Words::Fields::Field::get_IsDirty()
```


## Examples



Shows how to use special property for updating field result. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Give the document's built-in "Author" property value, and then display it with a field.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Update the property. The field still displays the old value.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Since the field's value is out of date, we can mark it as "dirty".
// This value will stay out of date until we update the field manually with the Field.Update() method.
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // If we save without calling an update method,
    // the field will keep displaying the out of date value in the output document.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // The LoadOptions object has an option to update all fields
    // marked as "dirty" when loading the document.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

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

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
