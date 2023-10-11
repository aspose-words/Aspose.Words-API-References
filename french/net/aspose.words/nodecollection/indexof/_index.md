---
title: NodeCollection.IndexOf
second_title: Référence de l'API Aspose.Words pour .NET
description: NodeCollection méthode. Renvoie lindex de base zéro du nœud spécifié.
type: docs
weight: 70
url: /fr/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

Renvoie l'index de base zéro du nœud spécifié.

```csharp
public int IndexOf(Node node)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| node | Node | Le nœud à localiser. |

### Return_Value

L'index de base zéro du nœud dans la collection, s'il est trouvé ; sinon, -1.

### Remarques

Cette méthode effectue une recherche linéaire ; par conséquent, le temps d'exécution moyen est proportionnel à[`Count`](../count/).

### Exemples

Montre comment obtenir l'index d'un nœud dans une collection.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.AreEqual(0, allTables.IndexOf(table));

Row row = table.Rows[2];

Assert.AreEqual(2, table.IndexOf(row));

Cell cell = row.LastCell;

Assert.AreEqual(4, row.IndexOf(cell));
```

### Voir également

* class [Node](../../node/)
* class [NodeCollection](../)
* espace de noms [Aspose.Words](../../nodecollection/)
* Assemblée [Aspose.Words](../../../)


