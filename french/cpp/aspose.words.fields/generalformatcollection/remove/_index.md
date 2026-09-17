---
title: "Aspose::Words::Fields::GeneralFormatCollection::Remove méthode"
linktitle: "Supprimer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::GeneralFormatCollection::Remove méthode. Supprime toutes les occurrences du format général spécifié de la collection en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.fields/generalformatcollection/remove/
---
## GeneralFormatCollection::Remove method


Supprime toutes les occurrences du format général spécifié de la collection.

```cpp
void Aspose::Words::Fields::GeneralFormatCollection::Remove(Aspose::Words::Fields::GeneralFormat item)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| élément | Aspose::Words::Fields::GeneralFormat | Un format général. |

## Exemples



Montre comment formater les résultats de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilisez un constructeur de document pour insérer un champ qui affiche un résultat sans aucun format appliqué.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// Nous pouvons appliquer un format au résultat d'un champ en utilisant les propriétés du champ.
// Voici trois types de formats que nous pouvons appliquer au résultat d'un champ.
// 1 -  Format numérique :
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Format date/heure :
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  Format général :
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(Aspose::Words::Fields::GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// Nous pouvons supprimer nos formats pour ramener le résultat du champ à sa forme originale.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## Voir aussi

* Enum [GeneralFormat](../../generalformat/)
* Class [GeneralFormatCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
