---
title: Table.FirstRow
linktitle: FirstRow
articleTitle: FirstRow
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FirstRow des tables, accédez sans effort au nœud de la première ligne pour une gestion simplifiée des données et des fonctionnalités de table améliorées.
type: docs
weight: 160
url: /fr/net/aspose.words.tables/table/firstrow/
---
## Table.FirstRow property

Renvoie le premier[`Row`](../../row/) nœud dans la table.

```csharp
public Row FirstRow { get; }
```

## Exemples

Montre comment supprimer la première et la dernière ligne de tous les tableaux d'un document.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

Montre comment combiner les lignes de deux tables en une seule.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Vous trouverez ci-dessous deux manières d’obtenir un tableau à partir d’un document.
// 1 - À partir de la collection « Tables » d'un nœud Body :
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilisation de la méthode « GetChild » :
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Ajouter toutes les lignes de la table actuelle à la suivante.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Supprimez le conteneur de table vide.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Voir également

* class [Row](../../row/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
