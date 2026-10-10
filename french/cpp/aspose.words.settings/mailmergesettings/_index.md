---
title: "classe Aspose::Words::Settings::MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Settings::MailMergeSettings. Spécifie toutes les informations de publipostage pour un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


Spécifie toutes les informations de fusion et publipostage pour un document. Pour en savoir plus, consultez l'article de documentation [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMergeSettings : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clear](./clear/)() | Efface les paramètres de publipostage de manière à ce que, lorsque le document est enregistré, aucun paramètre de publipostage ne soit sauvegardé et qu'il devienne un document normal. |
| [Clone](./clone/)() | Renvoie une copie profonde de cet objet. |
| [get_ActiveRecord](./get_activerecord/)() const | Spécifie l'index basé sur 1 de l'enregistrement de la source de données qui doit être affiché dans Microsoft Word. La valeur par défaut est 1. |
| [get_AddressFieldName](./get_addressfieldname/)() const | Spécifie la colonne de la source de données qui contient les adresses e-mail. La valeur par défaut est une chaîne vide. |
| [get_CheckErrors](./get_checkerrors/)() const | Spécifie le type de rapport d'erreurs qui doit être effectué par Microsoft Word lors d'un publipostage. La valeur par défaut est [Default](../mailmergecheckerrors/). |
| [get_ConnectString](./get_connectstring/)() const | Spécifie la chaîne de connexion utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide. |
| [get_DataSource](./get_datasource/)() const | Spécifie le chemin vers la source de données de publipostage. La valeur par défaut est une chaîne vide. |
| [get_DataType](./get_datatype/)() const | Spécifie le type de la source de données de publipostage et la méthode d'accès aux données. La valeur par défaut est [Default](../mailmergedatatype/). |
| [get_Destination](./get_destination/)() const | Spécifie comment Microsoft Word générera les résultats d'un publipostage. La valeur par défaut est [Default](../mailmergedestination/). |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | Spécifie comment une application effectuant le publipostage doit gérer les lignes vides dans les documents fusionnés résultant du publipostage. La valeur par défaut est **false**. |
| [get_HeaderSource](./get_headersource/)() const | Spécifie le chemin vers la source d'en-tête de publipostage. La valeur par défaut est une chaîne vide. |
| [get_LinkToQuery](./get_linktoquery/)() const | Pas sûr de celui-ci. La référence d'automatisation de Microsoft Word indique que cela spécifie que la requête est exécutée chaque fois que le document est ouvert dans Microsoft Word. Mais la spécification OOXML indique que cela spécifie que la requête contient une référence à un fichier de requête externe qui contient la requête réelle. La valeur par défaut est **false**. |
| [get_MailAsAttachment](./get_mailasattachment/)() const | Spécifie que les documents produits lors d'une opération de publipostage doivent être envoyés par e-mail en tant que pièce jointe plutôt que dans le corps du courriel réel. La valeur par défaut est **false**. |
| [get_MailSubject](./get_mailsubject/)() const | Spécifie le texte qui doit apparaître dans la ligne d'objet des e-mails ou fax produits lors du publipostage. La valeur par défaut est une chaîne vide. |
| [get_MainDocumentType](./get_maindocumenttype/)() const | Spécifie le type de document principal de publipostage. La valeur par défaut est [Default](../mailmergemaindocumenttype/). |
| [get_Odso](./get_odso/)() const | Obtient l'objet qui spécifie les paramètres de l'Office Data Source Object (ODSO). |
| [get_Query](./get_query/)() const | Contient la chaîne SQL (Structured Query Language) qui doit être exécutée contre la source de données externe spécifiée pour renvoyer l'ensemble des enregistrements qui seront importés dans le document lors de l'exécution du publipostage. La valeur par défaut est une chaîne vide. |
| [get_ViewMergedData](./get_viewmergeddata/)() const | Spécifie que Microsoft Word doit afficher les données de la source de données externe spécifiée où des champs de fusion ont été insérés (par ex. aperçu des données fusionnées). La valeur par défaut est **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | Spécifie l'index basé sur 1 de l'enregistrement de la source de données qui doit être affiché dans Microsoft Word. La valeur par défaut est 1. |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | Spécifie la colonne de la source de données qui contient les adresses e-mail. La valeur par défaut est une chaîne vide. |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | Spécifie le type de rapport d'erreurs qui doit être effectué par Microsoft Word lors d'un publipostage. La valeur par défaut est [Default](../mailmergecheckerrors/). |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | Spécifie la chaîne de connexion utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide. |
| [set_DataSource](./set_datasource/)(const System::String\&) | Spécifie le chemin vers la source de données de publipostage. La valeur par défaut est une chaîne vide. |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | Spécifie le type de la source de données de publipostage et la méthode d'accès aux données. La valeur par défaut est [Default](../mailmergedatatype/). |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | Spécifie comment Microsoft Word générera les résultats d'un publipostage. La valeur par défaut est [Default](../mailmergedestination/). |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | Spécifie comment une application effectuant le publipostage doit gérer les lignes vides dans les documents fusionnés résultant du publipostage. La valeur par défaut est **false**. |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | Spécifie le chemin vers la source d'en-tête de publipostage. La valeur par défaut est une chaîne vide. |
| [set_LinkToQuery](./set_linktoquery/)(bool) | Mutateur pour [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/). |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | Spécifie que les documents produits lors d'une opération de publipostage doivent être envoyés par e-mail en tant que pièce jointe plutôt que dans le corps du courriel réel. La valeur par défaut est **false**. |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | Spécifie le texte qui doit apparaître dans la ligne d'objet des e-mails ou fax produits lors du publipostage. La valeur par défaut est une chaîne vide. |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | Mutateur pour [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/). |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | Définit l'objet qui spécifie les paramètres de l'Office Data Source Object (ODSO). |
| [set_Query](./set_query/)(const System::String\&) | Contient la chaîne SQL (Structured Query Language) qui doit être exécutée contre la source de données externe spécifiée pour renvoyer l'ensemble des enregistrements qui seront importés dans le document lors de l'exécution du publipostage. La valeur par défaut est une chaîne vide. |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | Spécifie que Microsoft Word doit afficher les données de la source de données externe spécifiée où des champs de fusion ont été insérés (par ex. aperçu des données fusionnées). La valeur par défaut est **false**. |
| static [Type](./type/)() |  |
## Remarques


Vous pouvez utiliser cet objet pour spécifier une source de données de publipostage pour un document et ces informations (ainsi que les champs de données disponibles) apparaîtront dans Microsoft Word lorsque l'utilisateur ouvrira ce document. Vous pouvez également utiliser cet objet pour interroger les paramètres de publipostage que l'utilisateur a spécifiés dans Microsoft Word pour ce document.

Vous n'avez généralement pas besoin de créer des objets de cette classe directement car les paramètres de publipostage d'un document sont toujours disponibles via la propriété [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/).

Pour détecter si ce document est le document principal de fusion de courrier, vérifiez la valeur de la propriété [MainDocumentType](./get_maindocumenttype/).

Pour supprimer les paramètres de fusion de courrier et les informations de source de données d’un document, vous pouvez utiliser la méthode [Clear](./clear/). Aspose.Words n’écrira pas les paramètres de fusion de courrier dans un document si la propriété [MainDocumentType](./get_maindocumenttype/) est définie sur [NotAMergeDocument](../mailmergemaindocumenttype/) ou si la propriété [DataType](./get_datatype/) est définie sur [None](../mailmergedatatype/).

La meilleure façon d’apprendre à utiliser les propriétés de cet objet est de créer manuellement un document avec la source de données souhaitée dans Microsoft Word, puis d’ouvrir ce document avec Aspose.Words et d’examiner les propriétés des objets [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) et [Odso](./get_odso/). C’est une bonne approche à adopter si vous souhaitez, par exemple, apprendre à configurer une source de données de façon programmatique.

Aspose.Words conserve les informations de fusion de courrier lors du chargement, de l’enregistrement et de la conversion de documents entre différents formats, mais n’utilise pas ces informations lors de l’exécution de sa propre fusion de courrier avec l’objet [MailMerge](../../aspose.words.mailmerging/mailmerge/).

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
