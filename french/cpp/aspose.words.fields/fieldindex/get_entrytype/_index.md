---
title: "Aspose::Words::Fields::FieldIndex::get_EntryType méthode"
linktitle: "get_EntryType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldIndex::get_EntryType méthode. Obtient ou définit un type d'entrée d'index utilisé pour construire l'index en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/fieldindex/get_entrytype/
---
## FieldIndex::get_EntryType method


Obtient ou définit un type d'entrée d'index utilisé pour créer l'index.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_EntryType()
```


## Exemples



Montre comment créer un champ INDEX, puis utiliser des champs XE pour le remplir avec des entrées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche
// et la page contenant le champ XE sur la droite.
// Si les champs XE ont la même valeur dans leur propriété "Text",
// le champ INDEX les regroupera en une seule entrée.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Configurez le champ INDEX pour n'afficher que les champs XE qui se trouvent dans les limites
// d'un signet nommé "MainBookmark", et dont les propriétés "EntryType" ont la valeur "A".
// Pour les champs INDEX et XE, la propriété "EntryType" n'utilise que le premier caractère de sa valeur chaîne.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// Sur une nouvelle page, démarrez le signet avec un nom qui correspond à la valeur
// de la propriété "BookmarkName" du champ INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// Le champ INDEX récupérera cette entrée parce qu'elle se trouve à l'intérieur du signet,
// et son type d'entrée correspond également au type d'entrée du champ INDEX.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Insérez un champ XE qui n'apparaîtra pas dans l'INDEX parce que les types d'entrée ne correspondent pas.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Terminez le signet et insérez un champ XE ensuite.
// Il est du même type que le champ INDEX, mais n'apparaîtra pas
// car il se trouve en dehors des limites du signet.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```

## Voir aussi

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
