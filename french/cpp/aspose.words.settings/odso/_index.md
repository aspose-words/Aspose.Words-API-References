---
title: "Aspose::Words::Settings::Odso class"
linktitle: "Odso"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::Odso class. Spécifie les paramètres de l'Office Data Source Object (ODSO) pour une source de données de fusion et publipostage. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.settings/odso/
---
## Odso class


Spécifie les paramètres de l'Office Data Source Object (ODSO) pour une source de données de fusion et publipostage. Pour en savoir plus, consultez l'article de documentation [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class Odso : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Renvoie une copie profonde de cet objet. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | Spécifie le caractère qui doit être interprété comme le délimiteur de colonne utilisé pour séparer les colonnes dans les sources de données externes. La valeur par défaut est 0, ce qui signifie qu'aucun délimiteur de colonne n'est défini. |
| [get_DataSource](./get_datasource/)() const | Spécifie l'emplacement de la source de données externe à connecter à un document pour effectuer la fusion et publipostage. La valeur par défaut est une chaîne vide. |
| [get_DataSourceType](./get_datasourcetype/)() const | Spécifie le type de la source de données externe à connecter dans le cadre des informations de connexion ODSO pour cette fusion et publipostage. La valeur par défaut est [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | Obtient une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. Cet objet n'est jamais **null**. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | Spécifie qu'une application hôte doit traiter la première ligne de données de la source de données externe spécifiée comme une ligne d'en-tête contenant les noms de chaque colonne de la source. La valeur par défaut est **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | Obtient une collection d'objets qui spécifient l'inclusion/exclusion d'enregistrements individuels dans la fusion et publipostage. Cet objet n'est jamais **null**. |
| [get_TableName](./get_tablename/)() const | Spécifie l'ensemble particulier de données auquel une source doit être connectée au sein d'une source de données externe. La valeur par défaut est une chaîne vide. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | Spécifie la chaîne de connexion Universal Data Link (UDL) utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | Définisseur pour [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | Spécifie l'emplacement de la source de données externe à connecter à un document pour effectuer la fusion et publipostage. La valeur par défaut est une chaîne vide. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | Définisseur pour [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | Définit une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. Cet objet n'est jamais **null**. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | Définisseur pour [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | Définit une collection d'objets qui spécifient l'inclusion/l'exclusion d'enregistrements individuels dans la fusion de courrier. Cet objet n'est jamais **null**. |
| [set_TableName](./set_tablename/)(const System::String\&) | Spécifie l'ensemble particulier de données auquel une source doit être connectée au sein d'une source de données externe. La valeur par défaut est une chaîne vide. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | Spécifie la chaîne de connexion Universal Data Link (UDL) utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide. |
| static [Type](./type/)() |  |
## Remarques


ODSO semble être la façon « nouvelle » que les versions plus récentes de Microsoft Word préfèrent utiliser lors de la spécification de certains types de sources de données pour un document de fusion de courrier. ODSO est probablement apparu pour la première fois dans Microsoft Word 2000.

L'utilisation d'ODSO est mal documentée et la meilleure façon d'apprendre à utiliser les propriétés de cet objet est de créer manuellement un document avec la source de données souhaitée dans Microsoft Word, puis d'ouvrir ce document en utilisant Aspose.Words et d'examiner les propriétés des objets [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) et [Odso](../mailmergesettings/get_odso/). C'est une bonne approche à adopter si vous souhaitez apprendre, par exemple, à configurer une source de données de manière programmatique.

Vous n'avez généralement pas besoin de créer des objets de cette classe directement car les paramètres ODSO sont toujours disponibles via la propriété [Odso](../mailmergesettings/get_odso/).

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
