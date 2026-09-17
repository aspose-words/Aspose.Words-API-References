---
title: "Aspose::Words::Fields::FieldCitation classe"
linktitle: "FieldCitation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldCitation classe. Implémente le champ CITATION. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


Implémente le champ CITATION. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Obtient une valeur qui correspond à la valeur de l'élément **Tag** d'une autre source à inclure dans la citation. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Obtient l'ID de langue utilisé en conjonction avec le style bibliographique spécifié pour formater la citation dans le document. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_PageNumber](./get_pagenumber/)() | Obtient un numéro de page associé à la citation. |
| [get_Prefix](./get_prefix/)() | Obtient un préfixe qui est ajouté avant la citation. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_SourceTag](./get_sourcetag/)() | Obtient une valeur qui correspond à la valeur de l'élément **Tag** de la source à insérer. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Suffix](./get_suffix/)() | Obtient un suffixe qui est ajouté après la citation. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Obtient si les informations d'auteur sont supprimées de la citation. |
| [get_SuppressTitle](./get_suppresstitle/)() | Obtient si les informations de titre sont supprimées de la citation. |
| [get_SuppressYear](./get_suppressyear/)() | Obtient si les informations d'année sont supprimées de la citation. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [get_VolumeNumber](./get_volumenumber/)() | Obtient un numéro de volume associé à la citation. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Définit une valeur qui correspond à la valeur de l'élément **Tag** d'une autre source à inclure dans la citation. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Définit l'ID de langue utilisé en conjonction avec le style bibliographique spécifié pour formater la citation dans le document. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Définit un numéro de page associé à la citation. |
| [set_Prefix](./set_prefix/)(const System::String\&) | Définit un préfixe qui est ajouté avant la citation. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Définit une valeur qui correspond à la valeur de l'élément **Tag** de la source à insérer. |
| [set_Suffix](./set_suffix/)(const System::String\&) | Définit un suffixe qui est ajouté après la citation. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Définit si les informations d'auteur sont supprimées de la citation. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Définit si les informations de titre sont supprimées de la citation. |
| [set_SuppressYear](./set_suppressyear/)(bool) | Définit si les informations d'année sont supprimées de la citation. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Définit un numéro de volume associé à la citation. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
