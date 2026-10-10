---
title: "Méthode Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource"
linktitle: "GetChildDataSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource. Le moteur de fusion de courrier Aspose.Words invoque cette méthode lorsqu'il rencontre le début d'une région de fusion de courrier imbriquée en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


Le moteur de fusion de courrier Aspose.Words invoque cette méthode lorsqu'il rencontre le début d'une région de fusion de courrier imbriquée.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| tableName | System::String | Le nom de la région de fusion de courrier tel que spécifié dans le document modèle. Insensible à la casse. |

### ReturnValue

Un objet source de données qui fournira l'accès aux enregistrements de données de la table spécifiée.
## Remarques


Lorsque les moteurs de fusion de courrier Aspose.Words remplissent une région de fusion de courrier avec des données et rencontrent le début d'une région de fusion de courrier imbriquée sous la forme MERGEFIELD TableStart:TableName, ils invoquent [GetChildDataSource()](./) sur l'objet source de données actuel. Votre implémentation doit renvoyer un nouvel objet source de données qui fournira l'accès aux enregistrements enfants de l'enregistrement parent actuel. Aspose.Words utilisera la source de données renvoyée pour remplir la région de fusion de courrier imbriquée.

Voici les règles que l'implémentation de [GetChildDataSource()](./) doit suivre.

Si la table représentée par cet objet source de données possède une table enfant (détail) liée portant le nom spécifié, votre implémentation doit renvoyer un nouvel objet [IMailMergeDataSource](../) qui fournira l'accès aux enregistrements enfants de l'enregistrement actuel. Un exemple de cela est la relation Orders / OrderDetails. Supposons que l'objet [IMailMergeDataSource](../) actuel représente la table Orders et qu'il possède un enregistrement de commande actuel. Ensuite, Aspose.Words rencontre "MERGEFIELD TableStart:OrderDetails" dans le document et invoque [GetChildDataSource()](./). Vous devez créer et renvoyer un objet [IMailMergeDataSource](../) qui permettra à Aspose.Words d'accéder à l'enregistrement OrderDetails pour la commande actuelle.

Si cet objet source de données n'a pas de relation avec la table portant le nom spécifié, vous devez renvoyer un objet [IMailMergeDataSource](../) qui fournira l'accès à tous les enregistrements de la table spécifiée.

Si une table portant le nom spécifié n'existe pas, votre implémentation doit renvoyer **null**.

## Voir aussi

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
