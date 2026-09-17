---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource méthode"
linktitle: "GetDataSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource méthode. Le moteur de fusion de courrier Aspose.Words invoque cette méthode lorsqu'il rencontre le début d'une région de fusion de courrier de niveau supérieur en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


Le moteur de fusion de courrier Aspose.Words invoque cette méthode lorsqu'il rencontre le début d'une région de fusion de courrier de niveau supérieur.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| tableName | System::String | Le nom de la région de fusion de courrier tel que spécifié dans le document modèle. Insensible à la casse. |

### ReturnValue

Un objet source de données qui fournira l'accès aux enregistrements de données de la table spécifiée.
## Remarques


Lorsque les moteurs de fusion de courrier Aspose.Words remplissent un document avec des données et rencontrent MERGEFIELD TableStart:TableName, ils invoquent [GetDataSource()](./) sur cet objet. Votre implémentation doit renvoyer un nouvel objet source de données. Aspose.Words utilisera la source de données renvoyée pour remplir la région de fusion de courrier.

Si une source de données (table) avec le nom spécifié n'existe pas, votre implémentation doit renvoyer **null**.

## Voir aussi

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
