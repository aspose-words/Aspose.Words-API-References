---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: Aspose.Words pour .NET
description: Accédez à la propriété PreviousRow pour récupérer facilement le nœud de ligne précédent, améliorant ainsi votre navigation dans les données et rationalisant votre flux de travail de codage.
type: docs
weight: 100
url: /fr/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Obtient le précédent[`Row`](../) nœud.

```csharp
public Row PreviousRow { get; }
```

## Remarques

Cette méthode peut être utilisée lorsque vous avez besoin d'un accès typé aux lignes d'une table. Si a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) le nœud est trouvé dans une table au lieu d'une ligne, il est automatiquement parcouru pour obtenir une ligne contenue à l'intérieur.

## Exemples

Montre comment énumérer toutes les cellules du tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Énumérer toutes les cellules du tableau.
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
