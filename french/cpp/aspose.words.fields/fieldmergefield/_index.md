---
title: "Aspose::Words::Fields::FieldMergeField classe"
linktitle: "FieldMergeField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldMergeField classe. Implémente le champ MERGEFIELD. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 67000
url: /fr/cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


Implémente le champ MERGEFIELD. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field,
                        public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldName](./get_fieldname/)() | Obtient le nom d'un champ de données. |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | Renvoie uniquement le nom du champ de données. Tout préfixe est supprimé de la propriété prefix. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_IsMapped](./get_ismapped/)() | Obtient si ce champ est un champ mappé. |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | Obtient si la conversion de caractères doit être activée pour le formatage vertical. |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_TextAfter](./get_textafter/)() | Obtient le texte à insérer après le champ si le champ n'est pas vide. |
| [get_TextBefore](./get_textbefore/)() | Obtient le texte à insérer avant le champ si le champ n'est pas vide. |
| [get_Type](./get_type/)() const override | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_FieldName](./set_fieldname/)(const System::String\&) | Définit le nom d'un champ de données. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsMapped](./set_ismapped/)(bool) | Définit si ce champ est un champ mappé. |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | Définit si la conversion de caractères doit être activée pour le formatage vertical. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TextAfter](./set_textafter/)(const System::String\&) | Définit le texte à insérer après le champ si le champ n'est pas vide. |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | Définit le texte à insérer avant le champ si le champ n'est pas vide. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
