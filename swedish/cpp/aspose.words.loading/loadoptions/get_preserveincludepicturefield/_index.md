---
title: "Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField‑metod"
linktitle: "get_PreserveIncludePictureField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField‑metod. Hämtar eller anger om INCLUDEPICTURE‑fältet ska bevaras när Microsoft Word‑format läses. Standardvärdet är false i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


Hämtar eller anger om INCLUDEPICTURE-fältet ska bevaras när Microsoft Word-format läses. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## Anmärkningar


Som standard konverteras INCLUDEPICTURE‑fältet till ett formobjekt. Du kan åsidosätta detta om du behöver att fältet bevaras, till exempel om du vill uppdatera det programmässigt. Observera dock att detta tillvägagångssätt inte är vanligt för Aspose.Words. Använd det på egen risk.

Ett av de möjliga användningsfallen kan vara att använda ett MERGEFIELD som ett underfält för att dynamiskt ändra bildens källsökväg. I detta fall måste INCLUDEPICTURE bevaras i modellen.

## Exempel



Visar hur man bevarar eller kastar bort INCLUDEPICTURE‑fält när ett dokument laddas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // Vi kan sätta en flagga i ett LoadOptions‑objekt för att avgöra om alla INCLUDEPICTURE‑fält ska konverteras
    // till bildformer när ett dokument som innehåller dem laddas.
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

## Se även

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
