---
title: get_PreserveIncludePictureField
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is false.
type: docs
weight: 131
url: /cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions.get_PreserveIncludePictureField method


Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is false.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```


By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need the field to be preserved, for example, if you wish to update it programmatically. Note however that this approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.

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

