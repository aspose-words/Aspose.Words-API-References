---
title: IFieldDatabaseProvider.GetQueryResult
linktitle: GetQueryResult
articleTitle: GetQueryResult
second_title: Aspose.Words pour .NET
description: IFieldDatabaseProvider GetQueryResult méthode. Renvoie le résultat de la requête en C#.
type: docs
weight: 10
url: /fr/net/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider.GetQueryResult method

Renvoie le résultat de la requête.

```csharp
public FieldDatabaseDataTable GetQueryResult(string fileName, string connection, string query, 
    FieldDatabase field)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le chemin complet et le nom de fichier de la base de données spécifiés dans le commutateur de champ \d. |
| connection | String | La connexion aux données spécifiées dans le commutateur de champ \c. |
| query | String | Ensemble d'instructions SQL qui interrogent la base de données spécifiée dans le commutateur de champ \s. |
| field | FieldDatabase | Le champ en cours de mise à jour. |

### Return_Value

Le[`FieldDatabaseDataTable`](../../fielddatabasedatatable/) instance qui doit être utilisée pour la mise à jour du champ.

### Voir également

* class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* class [FieldDatabase](../../fielddatabase/)
* interface [IFieldDatabaseProvider](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
