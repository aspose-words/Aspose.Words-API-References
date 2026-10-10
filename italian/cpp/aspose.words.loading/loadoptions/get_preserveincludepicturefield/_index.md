---
title: "Metodo Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField"
linktitle: "get_PreserveIncludePictureField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField. Ottiene o imposta se conservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è false in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


Ottiene o imposta se conservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## Note


Per impostazione predefinita, il campo INCLUDEPICTURE viene convertito in un oggetto forma. Puoi sovrascrivere questo comportamento se hai bisogno che il campo sia conservato, ad esempio se desideri aggiornarlo programmaticamente. Nota però che questo approccio non è comune per Aspose.Words. Usalo a tuo rischio.

Uno dei possibili casi d'uso può essere l'utilizzo di un MERGEFIELD come campo figlio per modificare dinamicamente il percorso di origine dell'immagine. In questo caso è necessario che il campo INCLUDEPICTURE sia conservato nel modello.

## Esempi



Mostra come conservare o scartare i campi INCLUDEPICTURE durante il caricamento di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // Possiamo impostare un flag in un oggetto LoadOptions per decidere se convertire tutti i campi INCLUDEPICTURE
    // in forme immagine durante il caricamento di un documento che li contiene.
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

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
