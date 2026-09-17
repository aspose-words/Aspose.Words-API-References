---
title: "Méthode Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult"
linktitle: "GetQueryResult"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult. Retourne le résultat de la requête en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


Renvoie le résultat de la requête.

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | System::String | Le chemin complet et le nom de fichier de la base de données spécifiés dans le commutateur de champ \d. |
| connection | System::String | La connexion aux données spécifiées dans le commutateur de champ \c. |
| requête | System::String | L'ensemble des instructions SQL qui interrogent la base de données spécifiée dans le commutateur de champ \s. |
| champ | System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\> | Le champ en cours de mise à jour. |

### ReturnValue

L'instance [FieldDatabaseDataTable](../../fielddatabasedatatable/) qui doit être utilisée pour la mise à jour du champ.

## Voir aussi

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
