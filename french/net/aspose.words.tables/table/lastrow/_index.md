---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Table LastRow pour accéder facilement au nœud de ligne final de votre table, améliorant ainsi la gestion et l'efficacité des données.
type: docs
weight: 180
url: /fr/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Renvoie le dernier[`Row`](../../row/) nœud dans la table.

```csharp
public Row LastRow { get; }
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

### Voir également

* class [Row](../../row/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
