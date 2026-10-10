---
title: "Aspose::Words::Fields::FieldDatabase class"
linktitle: "FieldDatabase"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldDatabase class. Implémente le champ DATABASE. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words.fields/fielddatabase/
---
## FieldDatabase class


Implémente le champ DATABASE. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDatabase : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [FieldDatabase](./fielddatabase/)() |  |
| [get_Connection](./get_connection/)() | Obtient une connexion aux données. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_FileName](./get_filename/)() | Obtient le chemin complet et le nom de fichier de la base de données. |
| [get_FirstRecord](./get_firstrecord/)() | Obtient le numéro d'enregistrement entier du premier enregistrement de données à insérer. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_FormatAttributes](./get_formatattributes/)() | Obtient quels attributs du format doivent être appliqués au tableau. |
| [get_InsertHeadings](./get_insertheadings/)() | Obtient s'il faut insérer les noms de champs de la base de données comme en-têtes de colonne dans le tableau résultant. |
| [get_InsertOnceOnMailMerge](./get_insertonceonmailmerge/)() | Obtient s'il faut insérer les données au début d'une fusion. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LastRecord](./get_lastrecord/)() | Obtient le numéro d'enregistrement entier du dernier enregistrement de données à insérer. |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_Query](./get_query/)() | Obtient un ensemble d'instructions SQL qui interrogent la base de données. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_TableFormat](./get_tableformat/)() | Obtient le format qui doit être appliqué au résultat de la requête de la base de données. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_Connection](./set_connection/)(const System::String\&) | Définit une connexion aux données. |
| [set_FileName](./set_filename/)(const System::String\&) | Définit le chemin complet et le nom de fichier de la base de données. |
| [set_FirstRecord](./set_firstrecord/)(const System::String\&) | Définit le numéro d'enregistrement entier du premier enregistrement de données à insérer. |
| [set_FormatAttributes](./set_formatattributes/)(const System::String\&) | Définit quels attributs du format doivent être appliqués au tableau. |
| [set_InsertHeadings](./set_insertheadings/)(bool) | Définit s'il faut insérer les noms de champs de la base de données comme en-têtes de colonne dans le tableau résultant. |
| [set_InsertOnceOnMailMerge](./set_insertonceonmailmerge/)(bool) | Définit s'il faut insérer les données au début d'une fusion. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LastRecord](./set_lastrecord/)(const System::String\&) | Définit le numéro d'enregistrement entier du dernier enregistrement de données à insérer. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Query](./set_query/)(const System::String\&) | Définit un ensemble d'instructions SQL qui interrogent la base de données. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TableFormat](./set_tableformat/)(const System::String\&) | Définit le format qui doit être appliqué au résultat de la requête de base de données. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
