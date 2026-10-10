---
title: "Aspose::Words::Fields::FieldListNum::get_ListName méthode"
linktitle: "get_ListName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldListNum::get_ListName méthode. Obtient ou définit le nom de la définition de numérotation abstraite utilisée pour la numérotation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/fieldlistnum/get_listname/
---
## FieldListNum::get_ListName method


Obtient ou définit le nom de la définition de numérotation abstraite utilisée pour la numérotation.

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_ListName()
```


## Exemples



Montre comment numéroter les paragraphes avec les champs LISTNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les champs LISTNUM affichent un nombre qui s’incrémente à chaque champ LISTNUM.
// Ces champs offrent également une variété d’options qui nous permettent de les utiliser pour émuler des listes numérotées.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Les listes commencent à compter à 1 par défaut, mais nous pouvons définir ce nombre à une valeur différente, comme 0.
// Ce champ affichera "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// Les champs LISTNUM maintiennent des comptes séparés pour chaque niveau de liste.
// Insérer un champ LISTNUM dans le même paragraphe qu’un autre champ LISTNUM
// augmente le niveau de liste au lieu du compte.
// Le champ suivant continuera le compte que nous avons commencé ci‑dessus et affichera la valeur "1" au niveau de liste 1.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Ce champ démarrera un compte au niveau de liste 2. Il affichera la valeur "1".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Ce champ démarrera un compte au niveau de liste 3. Il affichera la valeur "1".
// Les différents niveaux de liste ont un formatage différent,
// ainsi ces champs combinés afficheront la valeur "1)a)i)".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Le prochain champ LISTNUM que nous insérons continuera le compte au niveau de liste
// sur lequel le champ LISTNUM précédent était.
// Nous pouvons utiliser la propriété "ListLevel" pour passer à un niveau de liste différent.
// Si ce champ LISTNUM restait au niveau de liste 3, il afficherait "ii)",
// mais, comme nous l’avons déplacé au niveau de liste 2, il poursuit le compte à ce niveau et affiche "b)".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Nous pouvons définir la propriété ListName pour que le champ émule un type de champ AUTONUM différent.
// "NumberDefault" émule AUTONUM, "OutlineDefault" émule AUTONUMOUT,
// et "LegalDefault" émule les champs AUTONUMLGL.
// Le nom de liste \"OutlineDefault\" avec 1 comme numéro de départ affichera \"I.\".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// Le ListName ne se transmet pas depuis le champ précédent, nous devrons donc le définir pour chaque nouveau champ.
// Ce champ continue le comptage avec un nom de liste différent et affiche \"II.\".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## Voir aussi

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
