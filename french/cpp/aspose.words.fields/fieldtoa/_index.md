---
title: "classe Aspose::Words::Fields::FieldToa"
linktitle: "FieldToa"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Fields::FieldToa. Implémente le champ TOA. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 104000
url: /fr/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


Implémente le champ TOA. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Obtient le nom du signet qui marque la partie du document utilisée pour construire le tableau. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_EntryCategory](./get_entrycategory/)() | Obtient la catégorie intégrale des entrées incluses dans le tableau. |
| [get_EntrySeparator](./get_entryseparator/)() | Obtient la séquence de caractères utilisée pour séparer une entrée du tableau des autorités et son numéro de page. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Obtient la séquence de caractères utilisée pour séparer deux numéros de page dans une liste de numéros de page. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Obtient la séquence de caractères utilisée pour séparer le début et la fin d'une plage de pages. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | Obtient si le formatage du texte de l'entrée dans le document doit être supprimé de l'entrée du tableau des autorités. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_SequenceName](./get_sequencename/)() | Obtient le nom d'une séquence dont le numéro est inclus avec le numéro de page. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Obtient la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [get_UseHeading](./get_useheading/)() | Obtient si l'en-tête de catégorie doit être inclus pour les entrées d'un tableau des autorités. |
| [get_UsePassim](./get_usepassim/)() | Obtient si l'on doit remplacer cinq références de page ou plus différentes vers la même autorité par \"passim\", qui est utilisé pour indiquer qu'un mot ou un passage apparaît fréquemment dans l'ouvrage cité. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Définit le nom du signet qui marque la partie du document utilisée pour construire le tableau. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Définit la catégorie intégrale des entrées incluses dans le tableau. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Définit la séquence de caractères utilisée pour séparer une entrée du tableau des autorités et son numéro de page. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Définit la séquence de caractères utilisée pour séparer deux numéros de page dans une liste de numéros de page. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Définit la séquence de caractères utilisée pour séparer le début et la fin d'une plage de pages. |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | Définit si le formatage du texte de l'entrée dans le document doit être supprimé de l'entrée du tableau des autorités. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Définit le nom d'une séquence dont le numéro est inclus avec le numéro de page. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page. |
| [set_UseHeading](./set_useheading/)(bool) | Définit si l'en-tête de catégorie doit être inclus pour les entrées d'un tableau des autorités. |
| [set_UsePassim](./set_usepassim/)(bool) | Définit si l'on doit remplacer cinq références de page ou plus différentes vers la même autorité par "passim", qui est utilisé pour indiquer qu'un mot ou un passage apparaît fréquemment dans l'ouvrage cité. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
