---
title: "Classe Aspose::Words::Fields::FieldIndex"
linktitle: "FieldIndex"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Fields::FieldIndex. Implémente le champ INDEX. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 59000
url: /fr/cpp/aspose.words.fields/fieldindex/
---
## FieldIndex class


Implémente le champ INDEX. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIndex : public Aspose::Words::Fields::Field,
                   public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Obtient ou définit le nom du signet qui marque la partie du document utilisée pour créer l'index. |
| [get_CrossReferenceSeparator](./get_crossreferenceseparator/)() | Obtient ou définit la séquence de caractères utilisée pour séparer les renvois croisés et les autres entrées. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_EntryType](./get_entrytype/)() | Obtient ou définit un type d'entrée d'index utilisé pour créer l'index. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_HasPageNumberSeparator](./get_haspagenumberseparator/)() | Obtient une valeur indiquant si le séparateur de numéro de page est remplacé via le code du champ. |
| [get_HasSequenceName](./get_hassequencename/)() | Obtient une valeur indiquant si une séquence doit être utilisée lors de la construction du résultat du champ. |
| [get_Heading](./get_heading/)() | Obtient ou définit un en-tête qui apparaît au début de chaque ensemble d'entrées pour une lettre donnée. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LanguageId](./get_languageid/)() | Obtient ou définit l'ID de langue utilisé pour générer l'index. |
| [get_LetterRange](./get_letterrange/)() | Obtient ou définit une plage de lettres à laquelle limiter l'index. |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_NumberOfColumns](./get_numberofcolumns/)() | Obtient ou définit le nombre de colonnes par page utilisé lors de la création de l'index. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Obtient ou définit la séquence de caractères utilisée pour séparer deux numéros de page dans une liste de numéros de page. |
| [get_PageNumberSeparator](./get_pagenumberseparator/)() | Obtient ou définit la séquence de caractères utilisée pour séparer une entrée d'index et son numéro de page. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Obtient ou définit la séquence de caractères utilisée pour séparer le début et la fin d'une plage de pages. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/)() | Obtient ou définit si les sous‑entrées sont placées sur la même ligne que l'entrée principale. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_SequenceName](./get_sequencename/)() | Obtient ou définit le nom d'une séquence dont le numéro est inclus avec le numéro de page. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [get_UseYomi](./get_useyomi/)() | Obtient ou définit s'il faut activer l'utilisation du texte yomi pour les entrées d'index. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_BookmarkName](./get_bookmarkname/). |
| [set_CrossReferenceSeparator](./set_crossreferenceseparator/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator](./get_crossreferenceseparator/). |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_EntryType](./get_entrytype/). |
| [set_Heading](./set_heading/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_Heading](./get_heading/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_LanguageId](./get_languageid/). |
| [set_LetterRange](./set_letterrange/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_LetterRange](./get_letterrange/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberOfColumns](./set_numberofcolumns/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_NumberOfColumns](./get_numberofcolumns/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_PageNumberListSeparator](./get_pagenumberlistseparator/). |
| [set_PageNumberSeparator](./set_pagenumberseparator/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator](./get_pagenumberseparator/). |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator](./get_pagerangeseparator/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RunSubentriesOnSameLine](./set_runsubentriesonsameline/)(bool) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_SequenceName](./get_sequencename/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_UseYomi](./set_useyomi/)(bool) | Définisseur pour [Aspose::Words::Fields::FieldIndex::get_UseYomi](./get_useyomi/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
