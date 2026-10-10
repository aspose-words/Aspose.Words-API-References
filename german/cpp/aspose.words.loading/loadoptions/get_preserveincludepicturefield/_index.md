---
title: "Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField Methode"
linktitle: "get_PreserveIncludePictureField"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField Methode. Gibt an, ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten erhalten bleiben soll, und legt dies fest. Der Standardwert ist false in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


Liest oder setzt, ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten erhalten bleiben soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## Hinweise


Standardmäßig wird das INCLUDEPICTURE‑Feld in ein Shape‑Objekt konvertiert. Sie können dies überschreiben, wenn das Feld erhalten bleiben soll, zum Beispiel wenn Sie es programmgesteuert aktualisieren möchten. Beachten Sie jedoch, dass dieser Ansatz bei Aspose.Words nicht üblich ist. Verwenden Sie ihn auf eigenes Risiko.

Ein möglicher Anwendungsfall könnte die Verwendung eines MERGEFIELD als untergeordnetes Feld sein, um den Quellpfad des Bildes dynamisch zu ändern. In diesem Fall muss das INCLUDEPICTURE im Modell erhalten bleiben.

## Beispiele



Zeigt, wie man INCLUDEPICTURE‑Felder beim Laden eines Dokuments beibehält oder verwirft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // Wir können ein Flag in einem LoadOptions‑Objekt setzen, um zu entscheiden, ob alle INCLUDEPICTURE‑Felder konvertiert werden sollen
    // in Bild‑Shapes, wenn ein Dokument geladen wird, das sie enthält.
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

## Siehe auch

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
