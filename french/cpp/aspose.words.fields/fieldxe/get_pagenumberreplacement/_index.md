---
title: "Aspose::Words::Fields::FieldXE::get_PageNumberReplacement méthode"
linktitle: "get_PageNumberReplacement"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldXE::get_PageNumberReplacement méthode. Obtient ou définit le texte utilisé à la place d'un numéro de page en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fields/fieldxe/get_pagenumberreplacement/
---
## FieldXE::get_PageNumberReplacement method


Obtient ou définit le texte utilisé à la place d'un numéro de page.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageNumberReplacement()
```


## Exemples



Montre comment définir des références croisées dans un champ INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page contenant le champ XE à droite.
// L'entrée INDEX collectera tous les champs XE avec des valeurs correspondantes dans la propriété "Text"
// en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Nous pouvons configurer un champ XE pour que son entrée INDEX affiche une chaîne au lieu d'un numéro de page.
// Tout d'abord, pour les entrées qui remplacent un numéro de page par une chaîne,
// spécifiez un séparateur personnalisé entre la valeur de la propriété Text du champ XE et la chaîne.
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// Insérez un champ XE, qui crée une entrée INDEX régulière affichant le numéro de page de ce champ,
// et n'invoque pas la valeur CrossReferenceSeparator.
// L'entrée pour ce champ XE affichera "Apple, 2".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// Insérez un autre champ XE à la page 3 et définissez une valeur pour la propriété PageNumberReplacement.
// Cette valeur apparaîtra à la place du numéro de la page sur laquelle se trouve ce champ,
// et la valeur CrossReferenceSeparator du champ INDEX apparaîtra devant elle.
// L'entrée pour ce champ XE affichera "Banana, see: Tropical fruit".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## Voir aussi

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
