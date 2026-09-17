---
title: "Aspose::Words::Fields::ToaCategories::idx_get méthode"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::ToaCategories::idx_get méthode. Obtient ou définit l'en-tête de catégorie par numéro de catégorie en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fields/toacategories/idx_get/
---
## ToaCategories::idx_get method


Obtient ou définit l'en-tête de catégorie par numéro de catégorie.

```cpp
System::String Aspose::Words::Fields::ToaCategories::idx_get(int32_t number)
```


## Exemples



Montre comment spécifier un ensemble de catégories pour les champs TOA.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les champs TOA peuvent filtrer leurs entrées par les catégories définies dans cette collection.
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// Cette collection de catégories est fournie avec des valeurs par défaut, que nous pouvons écraser avec des valeurs personnalisées.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// Nous pouvons toujours accéder aux valeurs par défaut via cette collection.
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// Insérez 2 champs TOA. Les champs TOA créent une entrée pour chaque champ TA dans le document.
// Utilisez le commutateur "\c" pour sélectionner l'index d'une catégorie dans notre collection.
//  Avec ce commutateur, un champ TOA ne récupérera que les entrées des champs TA qui
// ont également un commutateur "\c" avec un index de catégorie correspondant. Chaque champ TOA affichera également
// le nom de la catégorie vers laquelle son commutateur "\c" pointe.
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Insérez des entrées TOA sur 2 catégories. Notre premier champ TOA recevra une entrée,
// du deuxième champ TA dont le commutateur "\c" pointe également vers la première catégorie.
// Le deuxième champ TOA aura deux entrées provenant des deux autres champs TA.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## Voir aussi

* Class [ToaCategories](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
