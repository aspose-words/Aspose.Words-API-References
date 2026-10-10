---
title: "Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField 方法"
linktitle: "get_PreserveIncludePictureField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField 方法。获取或设置在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。默认值在 C++ 中为 false。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


获取或设置在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。默认值为 **false**。

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## 备注


默认情况下，INCLUDEPICTURE 字段会被转换为形状对象。如果需要保留该字段，例如希望以编程方式更新它，可以覆盖此行为。但请注意，这种做法在 Aspose.Words 中并不常见。使用风险自负。

一种可能的使用场景是将 MERGEFIELD 作为子字段，以动态更改图片的源路径。在这种情况下，需要在模型中保留 INCLUDEPICTURE。

## 示例



展示如何在加载文档时保留或丢弃 INCLUDEPICTURE 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // 我们可以在 LoadOptions 对象中设置一个标志，以决定是否将所有 INCLUDEPICTURE 字段转换
    // 在加载包含它们的文档时，将其转换为图像形状。
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

## 另见

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
