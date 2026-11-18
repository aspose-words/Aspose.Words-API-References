---
title: Aspose::Words::Fields::Field::Update method
linktitle: Update
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::Field::Update method. Performs the field update. Throws if the field is being updated already in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words.fields/field/update/
---
## Field::Update() method


Performs the field update. Throws if the field is being updated already.

```cpp
void Aspose::Words::Fields::Field::Update()
```

## Examples


Shows how to insert a field into a document using [FieldType](../../fieldtype/).

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
// In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode(), u" AUTHOR ");
ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode(), u" PAGE ");

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result(), u"John Doe");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result(), u"1");
}
else
{
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result(), System::String::Empty);
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result(), System::String::Empty);

    // We will need to update these fields using the update methods manually.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result(), u"John Doe");

    doc->UpdateFields();

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result(), u"1");
}
```

Shows how to format field results.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Use a document builder to insert a field that displays a result with no format applied.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(field->GetFieldCode(), u"= 2 + 3");
ASSERT_EQ(field->get_Result(), u"5");

// We can apply a format to a field's result using the field's properties.
// Below are three types of formats that we can apply to a field's result.
// 1 -  Numeric format:
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(field->GetFieldCode(), u"= 2 + 3 \\# $###.00");
ASSERT_EQ(field->get_Result(), u"$  5.00");

// 2 -  Date/time format:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(field->GetFieldCode(), (u"DATE \\@ \"dddd, MMMM dd, yyyy\""));
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  General format:
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(field->GetFieldCode(), u"= 25 + 33 \\* roman \\* Upper");
ASSERT_EQ(field->get_Result(), u"LVIII");
ASSERT_EQ(format->get_GeneralFormats()->get_Count(), 2);
ASSERT_EQ(format->get_GeneralFormats()->idx_get(0), GeneralFormat::LowercaseRoman);

// We can remove our formats to revert the field's result to its original form.
format->get_GeneralFormats()->Remove(GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(format->get_GeneralFormats()->get_Count(), 0);
field->Update();

ASSERT_EQ(field->GetFieldCode(), u"= 25 + 33  ");
ASSERT_EQ(field->get_Result(), u"58");
ASSERT_EQ(format->get_GeneralFormats()->get_Count(), 0);
```
## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::Update(bool) method


Performs a field update. Throws if the field is being updated already.

```cpp
void Aspose::Words::Fields::Field::Update(bool ignoreMergeFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | bool | If **true** then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |
## Examples


Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(SaveFormat::Docx));

    // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
    // into image shapes when loading a document that contains them.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_PreserveIncludePictureField(preserveIncludePictureField);

    doc = System::MakeObject<Aspose::Words::Document>(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        ASSERT_TRUE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == FieldType::FieldIncludePicture;
        }))));

        doc->UpdateFields();
        doc->Save(get_ArtifactsDir() + u"Field.PreserveIncludePicture.docx");
    }
    else
    {
        ASSERT_FALSE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == FieldType::FieldIncludePicture;
        }))));
    }
}
```
## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
