---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words pour .NET
description: Supprimez facilement des lignes de tableaux grâce à la méthode DeleteRow de DocumentBuilder. Simplifiez l'édition de vos documents et optimisez votre flux de travail !
type: docs
weight: 200
url: /fr/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Supprime une ligne d'une table.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| tableIndex | Int32 | L'index de la table. |
| rowIndex | Int32 | L'index de la ligne dans la table. |

### Return_Value

Le nœud de ligne qui vient d’être supprimé.

## Remarques

Si le curseur se trouve à l'intérieur de la ligne en cours de suppression, le curseur est déplacé vers la ligne suivante ou vers le paragraphe suivant après le tableau.

Si vous supprimez une ligne d'une table qui ne contient qu'une seule ligne, la table whole est supprimée.

Pour les paramètres d'index, lorsque l'index est supérieur ou égal à 0, il spécifie un index de début à partir de x000d, 0 étant le premier élément. Lorsque l'index est inférieur à 0, il spécifie un index de fin à partir de x000d, 1 étant le dernier élément.

## Exemples

Montre comment supprimer une ligne d'un tableau.

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

// Supprimez la première ligne du premier tableau du document.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Voir également

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
