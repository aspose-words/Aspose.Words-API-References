---
title: "Aspose::Words::Fields::FieldXE::get_Yomi méthode"
linktitle: "get_Yomi"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldXE::get_Yomi méthode. Obtient ou définit le yomi (premier caractère phonétique pour trier les index) de l'entrée d'index en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.fields/fieldxe/get_yomi/
---
## FieldXE::get_Yomi method


Obtient ou définit le yomi (premier caractère phonétique pour le tri des index) de l'entrée d'index.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Yomi()
```


## Exemples



Montre comment trier les entrées du champ INDEX phonétiquement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page contenant le champ XE à droite.
// L'entrée INDEX collectera tous les champs XE avec des valeurs correspondantes dans la propriété "Text"
// en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Le tableau INDEX trie automatiquement ses entrées par les valeurs de leurs propriétés Text par ordre alphabétique.
// Définissez le tableau INDEX pour trier les entrées phonétiquement en utilisant le Hiragana.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// Insérez 4 champs XE, qui apparaîtront comme des entrées dans le sommaire du champ INDEX.
// La propriété "Text" peut contenir l'orthographe d'un mot en Kanji, dont la prononciation peut être ambiguë,
// tandis que la version "Yomi" du mot indiquera exactement comment il se prononce en utilisant le Hiragana.
// Si nous définissons notre champ INDEX pour utiliser Yomi, il triera ces entrées
// par la valeur de leurs propriétés Yomi, au lieu de leurs valeurs Text.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Yomi.docx");
```

## Voir aussi

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
