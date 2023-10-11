---
title: Story.Tables
second_title: Référence de l'API Aspose.Words pour .NET
description: Story propriété. Obtient une collection de tables qui sont des enfants immédiats de lhistoire.
type: docs
weight: 50
url: /fr/net/aspose.words/story/tables/
---
## Story.Tables property

Obtient une collection de tables qui sont des enfants immédiats de l'histoire.

```csharp
public TableCollection Tables { get; }
```

### Exemples

Montre comment supprimer les première et dernière lignes de tous les tableaux d’un document.

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

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [Story](../)
* espace de noms [Aspose.Words](../../story/)
* Assemblée [Aspose.Words](../../../)


