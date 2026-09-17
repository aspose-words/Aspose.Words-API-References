---
title: "Aspose::Words::Fields::FieldAddressBlock classe"
linktitle: "FieldAddressBlock"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldAddressBlock classe. Implémente le champ ADDRESSBLOCK. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class


Implémente le champ ADDRESSBLOCK. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAddressBlock : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IFormattableMergeField
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [FieldAddressBlock](./fieldaddressblock/)() |  |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/)() | Obtient ou définit le nom du pays/région exclu. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/)() | Obtient ou définit si l'adresse doit être formatée selon le pays/région du destinataire tel que défini par POST*CODE (Union postale universelle 2006). |
| [get_IncludeCountryOrRegionName](./get_includecountryorregionname/)() | Obtient ou définit si le nom du pays/région doit être inclus. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LanguageId](./get_languageid/)() | Obtient ou définit l'ID de langue utilisé pour formater l'adresse. |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_NameAndAddressFormat](./get_nameandaddressformat/)() | Obtient ou définit le format du nom et de l'adresse. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetFieldNames](./getfieldnames/)() override | Renvoie une collection de noms de champs de fusion de courrier utilisés par le champ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_ExcludedCountryOrRegionName](./set_excludedcountryorregionname/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/). |
| [set_FormatAddressOnCountryOrRegion](./set_formataddressoncountryorregion/)(bool) | Mutateur pour [Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/). |
| [set_IncludeCountryOrRegionName](./set_includecountryorregionname/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldAddressBlock::get_IncludeCountryOrRegionName](./get_includecountryorregionname/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldAddressBlock::get_LanguageId](./get_languageid/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NameAndAddressFormat](./set_nameandaddressformat/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat](./get_nameandaddressformat/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
