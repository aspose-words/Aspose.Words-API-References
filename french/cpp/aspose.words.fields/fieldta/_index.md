---
title: "Aspose::Words::Fields::FieldTA classe"
linktitle: "FieldTA"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldTA classe. Implémente le champ TA. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 99000
url: /fr/cpp/aspose.words.fields/fieldta/
---
## FieldTA class


Implémente le champ TA. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldTA : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_EntryCategory](./get_entrycategory/)() | Obtient la catégorie d’entrée intégrale, qui est un nombre correspondant à l’ordre des catégories. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsBold](./get_isbold/)() | Obtient si le formatage en gras doit être appliqué au numéro de page pour l’entrée. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsItalic](./get_isitalic/)() | Obtient si le formatage en italique doit être appliqué au numéro de page pour l’entrée. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_LongCitation](./get_longcitation/)() | Obtient la citation longue de l'entrée. |
| [get_PageRangeBookmarkName](./get_pagerangebookmarkname/)() | Obtient le nom du signet qui marque une plage de pages insérée comme numéro de page de l'entrée. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_ShortCitation](./get_shortcitation/)() | Obtient la citation courte de l'entrée. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Définit la catégorie d'entrée intégrale, qui est un nombre correspondant à l'ordre des catégories. |
| [set_IsBold](./set_isbold/)(bool) | Définit si le format gras doit être appliqué au numéro de page de l'entrée. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsItalic](./set_isitalic/)(bool) | Définit si le format italique doit être appliqué au numéro de page de l'entrée. |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LongCitation](./set_longcitation/)(const System::String\&) | Définit la citation longue de l'entrée. |
| [set_PageRangeBookmarkName](./set_pagerangebookmarkname/)(const System::String\&) | Définit le nom du signet qui marque une plage de pages insérée comme numéro de page de l'entrée. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ShortCitation](./set_shortcitation/)(const System::String\&) | Définit la citation courte de l'entrée. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
