---
title: "Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator méthode"
linktitle: "get_HasPageNumberSeparator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator méthode. Obtient une valeur indiquant si le séparateur de numéro de page est remplacé via le code du champ en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fields/fieldindex/get_haspagenumberseparator/
---
## FieldIndex::get_HasPageNumberSeparator method


Obtient une valeur indiquant si le séparateur de numéro de page est remplacé via le code du champ.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator()
```


## Exemples



Montre comment modifier le séparateur de numéro de page dans un champ INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page contenant le champ XE à droite.
// L'entrée INDEX regroupera les champs XE avec des valeurs correspondantes dans la propriété "Text".
// en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Si notre champ INDEX possède une entrée pour un groupe de champs XE,
// cette entrée affichera le numéro de chaque page contenant un champ XE appartenant à ce groupe.
// Nous pouvons définir des séparateurs personnalisés pour personnaliser l'apparence de ces numéros de page.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageNumberListSeparator(u" & ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\l \" & \"", index->GetFieldCode());
ASSERT_TRUE(index->get_HasPageNumberSeparator());

// Après avoir inséré ces champs XE, le champ INDEX affichera "Première entrée, sur la page(s) 2 & 3 & 4".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

ASSERT_EQ(u" XE  \"First entry\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageNumberList.docx");
```

## Voir aussi

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
