---
title: "Méthode Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine. Obtient ou définit si les sous‑entrées sont placées sur la même ligne que l’entrée principale en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


Obtient ou définit si les sous‑entrées sont placées sur la même ligne que l'entrée principale.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## Exemples



Montre comment travailler avec les sous‑entrées dans un champ INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page contenant le champ XE à droite.
// L'entrée INDEX collectera tous les champs XE avec des valeurs correspondantes dans la propriété "Text"
// en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// Champs XE qui possèdent une propriété Text dont la valeur devient le titre de l’entrée INDEX.
// Si cette valeur contient deux segments de chaîne séparés par un deux‑points (le délimiteur :) sera traité par l’entrée INDEX,
// le premier segment est le titre, et le second segment deviendra le sous‑titre.
// Le champ INDEX regroupe d’abord les entrées par ordre alphabétique, puis, s’il existe plusieurs champs XE avec le même
// titres, le champ INDEX les sous‑regroupera davantage selon les valeurs de ces titres.
// Il peut y avoir plusieurs niveaux de sous‑groupement, selon le nombre de fois
// que les propriétés Text des champs XE sont segmentées de cette manière.
// Par défaut, un groupe d’entrées d’un champ INDEX créera une nouvelle ligne pour chaque sous‑titre de ce groupe.
// Nous pouvons définir le drapeau RunSubentriesOnSameLine sur true pour conserver le titre,
// et chaque sous‑titre du groupe sur une seule ligne à la place, ce qui rendra le champ INDEX plus compact.
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// Insérez deux champs XE, chacun sur une nouvelle page, et avec le même titre nommé "Heading 1",
// que le champ INDEX utilisera pour les regrouper.
// Si RunSubentriesOnSameLine est false, alors le tableau INDEX créera trois lignes :
// une ligne pour le titre de regroupement "Heading 1", et une ligne supplémentaire pour chaque sous‑titre.
// Si RunSubentriesOnSameLine est true, alors le tableau INDEX créera une ligne unique
// d’entrée qui englobe le titre et tous les sous‑titres.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 1");

ASSERT_EQ(u" XE  \"Heading 1:Subheading 1\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 2");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + System::String::Format(u"Field.INDEX.XE.Subheading.docx"));
```

## Voir aussi

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
