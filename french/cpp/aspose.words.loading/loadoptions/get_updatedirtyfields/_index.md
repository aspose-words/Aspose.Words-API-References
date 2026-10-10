---
title: "Méthode Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields"
linktitle: "get_UpdateDirtyFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields. Spécifie s'il faut mettre à jour les champs avec l'attribut dirty en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.loading/loadoptions/get_updatedirtyfields/
---
## LoadOptions::get_UpdateDirtyFields method


Spécifie s'il faut mettre à jour les champs avec l'attribut **dirty**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields() const
```


## Exemples



Montre comment utiliser la propriété spéciale pour mettre à jour le résultat du champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fournissez la valeur de la propriété intégrée "Author" du document, puis affichez‑la avec un champ.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Mettez à jour la propriété. Le champ affiche toujours l'ancienne valeur.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Comme la valeur du champ est obsolète, nous pouvons la marquer comme "dirty".
// Cette valeur restera obsolète jusqu'à ce que nous mettions à jour le champ manuellement avec la méthode Field.Update().
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // Si nous enregistrons sans appeler une méthode de mise à jour,
    // le champ continuera d'afficher la valeur obsolète dans le document de sortie.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // L'objet LoadOptions possède une option pour mettre à jour tous les champs
    // marqués comme "dirty" lors du chargement du document.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // La mise à jour des champs dirty de cette façon définit automatiquement leur drapeau "IsDirty" sur false.
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## Voir aussi

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
