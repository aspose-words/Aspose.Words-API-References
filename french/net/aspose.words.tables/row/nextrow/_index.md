---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words pour .NET
description: Row NextRow propriété. Obtient le suivantRow nœud en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Obtient le suivant[`Row`](../) nœud.

```csharp
public Row NextRow { get; }
```

## Remarques

La méthode peut être utilisée lorsque vous devez avoir un accès typé aux lignes du tableau. Si a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)le nœud se trouve dans une table au lieu d'une ligne, il est automatiquement parcouru pour obtenir une ligne contenue à l'intérieur.

## Exemples

Montre comment énumérer toutes les cellules du tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Énumère toutes les cellules du tableau.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Voir également

* class [Row](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
