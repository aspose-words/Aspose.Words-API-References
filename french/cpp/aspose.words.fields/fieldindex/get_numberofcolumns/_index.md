---
title: "Aspose::Words::Fields::FieldIndex::get_NumberOfColumns méthode"
linktitle: "get_NumberOfColumns"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldIndex::get_NumberOfColumns méthode. Obtient ou définit le nombre de colonnes par page utilisées lors de la création de l'index en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.fields/fieldindex/get_numberofcolumns/
---
## FieldIndex::get_NumberOfColumns method


Obtient ou définit le nombre de colonnes par page utilisé lors de la création de l'index.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_NumberOfColumns()
```


## Exemples



Montre comment remplir un champ INDEX avec des entrées en utilisant des champs XE, et également modifier son apparence.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page contenant le champ XE à droite.
// Si les champs XE ont la même valeur dans leur propriété "Text",
// le champ INDEX les regroupera en une seule entrée.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Définir la valeur de cette propriété sur "A" regroupera toutes les entrées par leur première lettre,
// et placera cette lettre en majuscules au-dessus de chaque groupe.
index->set_Heading(u"A");

// Définissez le tableau créé par le champ INDEX pour s'étendre sur 2 colonnes.
index->set_NumberOfColumns(u"2");

// Définissez que toute entrée dont la lettre de départ est en dehors de la plage de caractères "a-c" soit omise.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// Les deux prochains champs XE apparaîtront sous le titre "A",
// avec leurs styles de texte respectifs également appliqués à leurs numéros de page.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Les deux prochains champs XE seront sous les titres "B" et "C" dans la table des matières des champs INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// Les champs INDEX trient toutes les entrées par ordre alphabétique, ainsi cette entrée apparaîtra sous "A" avec les deux autres.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Cette entrée n'apparaîtra pas car elle commence par la lettre "D",
// qui est en dehors de la plage de caractères "a-c" définie par la propriété LetterRange du champ INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Voir aussi

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
