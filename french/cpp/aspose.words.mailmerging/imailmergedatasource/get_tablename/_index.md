---
title: "Méthode Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName"
linktitle: "get_TableName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName. Retourne le nom de la source de données en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.mailmerging/imailmergedatasource/get_tablename/
---
## IMailMergeDataSource::get_TableName method


Renvoie le nom de la source de données.

```cpp
virtual System::String Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName()=0
```


### ReturnValue

Le nom de la source de données. Chaîne vide si la source de données n'a pas de nom.
## Remarques


Si vous implémentez [IMailMergeDataSource](../), renvoyez le nom de la source de données depuis cette propriété.

Aspose.Words utilise ce nom pour le faire correspondre au nom de la région de fusion de courrier spécifié dans le document modèle. La comparaison entre le nom de la source de données et le nom de la région de fusion de courrier n'est pas sensible à la casse.

## Voir aussi

* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
