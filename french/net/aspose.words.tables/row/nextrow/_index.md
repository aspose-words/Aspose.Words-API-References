---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words pour .NET
description: Découvrez la propriété NextRow pour accéder sans effort au nœud de ligne suivant, améliorant ainsi votre expérience de navigation et de gestion des données.
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
