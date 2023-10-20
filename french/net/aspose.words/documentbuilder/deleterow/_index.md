---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words pour .NET
description: DocumentBuilder DeleteRow méthode. Supprime une ligne dun tableau en C#.
type: docs
weight: 200
url: /fr/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Supprime une ligne d'un tableau.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| tableIndex | Int32 | L'index du tableau. |
| rowIndex | Int32 | L'index de la ligne dans le tableau. |

### Return_Value

Le nœud de ligne qui vient d'être supprimé.

## Remarques

Si le curseur se trouve à l'intérieur de la ligne en cours de suppression, le curseur est déplacé vers la ligne suivante ou vers le paragraphe suivant après le tableau.

Si vous supprimez une ligne d'une table qui ne contient qu'une seule ligne, la table Whole est supprimée.

Pour les paramètres d'index, lorsque l'index est supérieur ou égal à 0, il spécifie un index from au début, 0 étant le premier élément. Lorsque l'index est inférieur à 0, il spécifie un index from à la fin, -1 étant le dernier élément.

## Exemples

Montre comment supprimer une ligne d’un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// Supprime la première ligne du premier tableau du document.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Voir également

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
