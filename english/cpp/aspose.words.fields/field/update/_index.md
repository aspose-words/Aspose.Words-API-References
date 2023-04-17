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



Shows how to insert a field into a document using FieldType. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
// In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // We will need to update these fields using the update methods manually.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```


Shows how to format field results. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Use a document builder to insert a field that displays a result with no format applied.
SharedPtr<Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// We can apply a format to a field's result using the field's properties.
// Below are three types of formats that we can apply to a field's result.
// 1 -  Numeric format:
SharedPtr<FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Date/time format:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << "Today's date, in " << format->get_DateTimeFormat() << " format:\n\t" << field->get_Result() << std::endl;

// 3 -  General format:
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(GeneralFormat::Upper);
field->Update();

int index = 0;
{
    SharedPtr<System::Collections::Generic::IEnumerator<GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// We can remove our formats to revert the field's result to its original form.
format->get_GeneralFormats()->Remove(GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto includePicture = System::DynamicCast<FieldIncludePicture>(builder->InsertField(FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(ImageDir + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, MakeObject<OoxmlSaveOptions>(SaveFormat::Docx));

    // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
    // into image shapes when loading a document that contains them.
    auto loadOptions = MakeObject<Loading::LoadOptions>();
    loadOptions->set_PreserveIncludePictureField(preserveIncludePictureField);

    doc = MakeObject<Document>(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        ASSERT_TRUE(doc->get_Range()->get_Fields()->LINQ_Any([](SharedPtr<Field> f) { return f->get_Type() == FieldType::FieldIncludePicture; }));

        doc->UpdateFields();
        doc->Save(ArtifactsDir + u"Field.PreserveIncludePicture.docx");
    }
    else
    {
        ASSERT_FALSE(doc->get_Range()->get_Fields()->LINQ_Any([](SharedPtr<Field> f) { return f->get_Type() == FieldType::FieldIncludePicture; }));
    }
}
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
