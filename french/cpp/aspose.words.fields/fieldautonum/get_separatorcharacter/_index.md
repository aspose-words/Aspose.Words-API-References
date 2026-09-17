---
title: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter method"
linktitle: "get_SeparatorCharacter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter method. Obtient ou définit le caractère séparateur à utiliser en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


Obtient ou définit le caractère séparateur à utiliser.

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## Exemples



Montre comment numéroter les paragraphes en utilisant des champs autonum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Chaque champ AUTONUM affiche la valeur actuelle d’un compteur continu de champs AUTONUM,
// nous permettant de numéroter automatiquement les éléments comme dans une liste numérotée.
// Ce champ affichera le nombre "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// Le caractère séparateur, qui apparaît dans le résultat du champ immédiatement après le nombre, est un point par défaut.
// Si nous laissons cette propriété nulle, notre deuxième champ AUTONUM affichera "2." dans le document.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// Nous pouvons définir cette propriété pour appliquer le premier caractère de sa chaîne comme nouveau caractère séparateur.
// Dans ce cas, notre champ AUTONUM affichera maintenant "2:".
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## Voir aussi

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
