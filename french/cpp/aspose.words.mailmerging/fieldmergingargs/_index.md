---
title: "Aspose::Words::MailMerging::FieldMergingArgs classe"
linktitle: "FieldMergingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::FieldMergingArgs classe. Fournit des données pour l'événement MergeField. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


Fournit des données pour l'événement **MergeField**. Pour en savoir plus, consultez l'article de documentation [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Renvoie l'objet [Document](../fieldmergingargsbase/get_document/) pour lequel la fusion de courrier est effectuée. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Obtient le nom du champ de fusion tel qu’il est spécifié dans le document. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Obtient l'objet qui représente le champ de fusion actuel. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Obtient le nom du champ de fusion dans la source de données. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Obtient la valeur du champ à partir de la source de données. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Obtient l'index basé sur zéro de l'enregistrement qui est fusionné. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Obtient le nom de la table de données pour l'opération de fusion actuelle ou une chaîne vide si le nom n'est pas disponible. |
| [get_Text](./get_text/)() const | Obtient ou définit le texte qui sera inséré dans le document pour le champ de fusion actuel. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Définit la valeur du champ à partir de la source de données. |
| [set_Text](./set_text/)(const System::String\&) | Définisseur pour [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/). |
| static [Type](./type/)() |  |
## Remarques


L'événement **MergeField** se produit pendant la fusion de courrier lorsqu'un champ de fusion simple est rencontré dans le document. Vous pouvez répondre à cet événement pour renvoyer du texte que le moteur de fusion de courrier insérera dans le document.

## Voir aussi

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
