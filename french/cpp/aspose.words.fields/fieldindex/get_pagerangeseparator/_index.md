---
title: "Méthode Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator"
linktitle: "get_PageRangeSeparator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator. Obtient ou définit la séquence de caractères utilisée pour séparer le début et la fin d’une plage de pages en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.fields/fieldindex/get_pagerangeseparator/
---
## FieldIndex::get_PageRangeSeparator method


Obtient ou définit la séquence de caractères utilisée pour séparer le début et la fin d'une plage de pages.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator()
```


## Exemples



Montre comment spécifier les pages couvertes par un signet comme une plage de pages pour une entrée de champ INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page contenant le champ XE à droite.
// L'entrée INDEX collectera tous les champs XE avec des valeurs correspondantes dans la propriété "Text"
// en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Pour les entrées INDEX qui affichent des plages de pages, nous pouvons spécifier une chaîne séparatrice
// qui apparaîtra entre le numéro de la première page et le numéro de la dernière.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// Si un champ XE nomme un signet en utilisant la propriété PageRangeBookmarkName,
// son entrée INDEX affichera la plage de pages que le signet couvre
// au lieu du numéro de la page contenant le champ XE.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// Insérez un signet qui commence à la page 3 et se termine à la page 5.
// L'entrée INDEX du champ XE qui fait référence à ce signet affichera cette plage de pages.
// Dans notre tableau, l'entrée INDEX affichera "My entry, on page(s) 3 to 5".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## Voir aussi

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
