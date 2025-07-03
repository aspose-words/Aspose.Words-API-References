---
title: Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField method
linktitle: get_PreserveIncludePictureField
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField method. Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is false in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is **false**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## Remarks


By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need the field to be preserved, for example, if you wish to update it programmatically. Note however that this approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.

## Examples



Shows how to preserve or discard INCLUDEPICTURE fields when loading a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
    // into image shapes when loading a document that contains them.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_PreserveIncludePictureField(preserveIncludePictureField);

    doc = System::MakeObject<Aspose::Words::Document>(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        ASSERT_TRUE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == Aspose::Words::Fields::FieldType::FieldIncludePicture;
        }))));

        doc->UpdateFields();
        doc->Save(get_ArtifactsDir() + u"Field.PreserveIncludePicture.docx");
    }
    else
    {
        ASSERT_FALSE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == Aspose::Words::Fields::FieldType::FieldIncludePicture;
        }))));
    }
}
```

## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
