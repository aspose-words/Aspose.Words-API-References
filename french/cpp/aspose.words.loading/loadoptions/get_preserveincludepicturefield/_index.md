---
title: "Méthode Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField"
linktitle: "get_PreserveIncludePictureField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField. Obtient ou définit si le champ INCLUDEPICTURE doit être conservé lors de la lecture des formats Microsoft Word. La valeur par défaut est false en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## Remarques


Par défaut, le champ INCLUDEPICTURE est converti en objet forme. Vous pouvez le remplacer si vous avez besoin que le champ soit conservé, par exemple si vous souhaitez le mettre à jour programmatiquement. Notez toutefois que cette approche n'est pas courante pour Aspose.Words. Utilisez‑la à vos propres risques.

Un des cas d'utilisation possibles peut consister à utiliser un MERGEFIELD comme champ enfant pour modifier dynamiquement le chemin source de l'image. Dans ce cas, vous devez que le champ INCLUDEPICTURE soit conservé dans le modèle.

## Exemples



Montre comment conserver ou ignorer les champs INCLUDEPICTURE lors du chargement d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // Nous pouvons définir un indicateur dans un objet LoadOptions pour décider s'il faut convertir tous les champs INCLUDEPICTURE
    // en formes image lors du chargement d'un document qui les contient.
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

## Voir aussi

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
