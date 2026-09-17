---
title: "Aspose::Words::Fields::FieldIndex::get_HasSequenceName méthode"
linktitle: "get_HasSequenceName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldIndex::get_HasSequenceName méthode. Obtient une valeur indiquant si une séquence doit être utilisée lors de la construction du résultat du champ en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.fields/fieldindex/get_hassequencename/
---
## FieldIndex::get_HasSequenceName method


Obtient une valeur indiquant si une séquence doit être utilisée lors de la construction du résultat du champ.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_HasSequenceName()
```


## Exemples



Montre comment diviser un document en parties en combinant les champs INDEX et SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page contenant le champ XE à droite.
// Si les champs XE ont la même valeur dans leur propriété "Text",
// le champ INDEX les regroupera en une seule entrée.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Dans la propriété SequenceName, nommez une séquence de champ SEQ. Chaque entrée de ce champ INDEX affichera désormais également
// le numéro auquel le compteur de séquence se trouve à l’emplacement du champ XE qui a créé cette entrée.
index->set_SequenceName(u"MySequence");

// Définissez le texte qui entourera la séquence et les numéros de page pour expliquer leur signification à l’utilisateur.
// Une entrée créée avec cette configuration affichera quelque chose comme "MySequence at 1 on page 1" à son numéro de page.
// PageNumberSeparator et SequenceSeparator ne peuvent pas dépasser 15 caractères.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
// Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique.
// identifié par la propriété "SequenceIdentifier" du champ SEQ.
// Insérez un champ SEQ qui déplace la séquence "MySequence" à 1.
// Ce champ n’est pas différent du texte normal du document. Il n’apparaîtra pas dans la table des matières d’un champ INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// Insérez un champ XE qui créera une entrée dans le champ INDEX.
// Puisque "MySequence" est à 1 et que ce champ XE se trouve à la page 2, ainsi que les séparateurs personnalisés que nous avons définis ci‑dessus,
// l'entrée INDEX de ce champ affichera "Cat" sur le côté gauche, et "MySequence at 1 on page 2" à droite.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// Insérez un saut de page et utilisez les champs SEQ pour faire avancer "MySequence" à 3.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// Insérez un champ XE avec la même propriété Text que celui ci‑dessus.
// L'entrée INDEX regroupera les champs XE avec des valeurs correspondantes dans la propriété "Text".
// en une seule entrée plutôt que de créer une entrée pour chaque champ XE.
// Puisque nous sommes à la page 2 avec "MySequence" à 3, ", 3 on page 3" sera ajouté à la même entrée INDEX que ci‑dessus.
// La partie numéro de page de cette entrée INDEX affichera maintenant "MySequence at 1 on page 2, 3 on page 3".
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// Insérez un champ XE avec une nouvelle valeur unique pour la propriété Text.
// Cela ajoutera une nouvelle entrée, avec MySequence à 3 à la page 4.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## Voir aussi

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
