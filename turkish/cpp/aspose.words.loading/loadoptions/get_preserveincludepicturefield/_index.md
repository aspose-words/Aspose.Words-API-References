---
title: "Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField yöntemi"
linktitle: "get_PreserveIncludePictureField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField yöntemi. Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer C++'ta false'tur."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## Açıklamalar


Varsayılan olarak, INCLUDEPICTURE alanı bir şekil nesnesine dönüştürülür. Alanın korunması gerektiğinde, örneğin programlı olarak güncellemek istediğinizde, bunu geçersiz kılabilirsiniz. Ancak bu yaklaşım Aspose.Words için yaygın değildir. Kendi sorumluluğunuzda kullanın.

Olası kullanım senaryolarından biri, resmi dinamik olarak kaynak yolunu değiştirmek için bir alt alan olarak MERGEFIELD kullanmak olabilir. Bu durumda modeli içinde INCLUDEPICTURE alanının korunması gerekir.

## Örnekler



Bir belge yüklenirken INCLUDEPICTURE alanlarını nasıl koruyup atılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // Tüm INCLUDEPICTURE alanlarını dönüştürüp dönüştürmeyeceğimizi belirlemek için bir LoadOptions nesnesinde bir bayrak ayarlayabiliriz
    // içeren bir belge yüklendiğinde görüntü şekillerine.
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

## Ayrıca Bakınız

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
